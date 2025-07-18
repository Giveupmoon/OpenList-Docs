<script lang="ts" setup>
  import { computed, ref } from 'vue'
  import { useI18n } from 'vue-i18n'

  export interface ValaxyAddon {
    icon: string
    name: string
    author: string | string[]
    repo: string
    desc: string
    desc_zh: string
    siteImage: string
    siteExampleUrl?: string
    tags?: string[]
  }

  const props = withDefaults(
    defineProps<{
      addons: ValaxyAddon[]
    }>(),
    {}
  )

  const { t } = useI18n()
  const keyword = ref('')
  const filteredAddons = computed(() => {
    return props.addons
      .filter(
        item => item.name.includes(keyword.value) || item.tags?.some(t => t.includes(keyword.value))
      )
      .map(item => {
        if (typeof item.author === 'string') return { ...item, author: [item.author] }

        return item
      })
  })

  function handleTagClick(tag: string) {
    keyword.value = tag
  }
</script>

<template>
  <div class="relative my-4 flex-center" flex="~" rounded>
    <div class="i-ri-search-line absolute text-slate-400 left-0 pl-12" />
    <input
      v-model="keyword"
      :placeholder="t('gallery.tip')"
      pl-10
      pr-4
      class="focus:border-purple-500 b-2 w-full h-12"
      dark="border-dark-200"
      bg="bg-white dark:bg-dark-500"
      rounded-lg
      transition
      type="text"
      name="search"
    />
  </div>
  <ul class="m-0! p-0! sm:grid-cols-1 lg:grid-cols-2 grid" gap="4">
    <li v-for="(addon, i) in filteredAddons" :key="i" class="w-full list-none m-0!">
      <AddonGalleryCard :addon="addon" @tag-click="handleTagClick" />
    </li>
  </ul>
</template>
