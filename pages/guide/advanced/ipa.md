---
title:
  en: IPA install
  zh-CN: IPA 安装
categories:
  - guide
  - advanced
top: 70
---

## 1. IPA native installation { lang="en" }

## 1. IPA原生安装 { lang="zh-CN" }

::: en
You can directly upload the ipa file.
But for **ios>=16**, you need to name the ipa file: `original file name@bundle-identifier.ipa`, that is, you need to add `@bundle-identifier` on the original basis, in which `bundle-identifier` is the `CFBundleIdentifier` of Info.plist in the IPA package. Such as:

- aszs@rn.notes.best.ipa
  Recommended to use [ipa-renamer](https://github.com/Xhofe/ipa-renamer) to rename your ipa files automatically and quickly.
- If you are a mobile phone user, you can also rename the IPA file, but you must know the format mentioned above, but there is no mobile phone renaming software, please solve it yourself...

:::

::: zh-CN
直接上传 ipa 文件即可。
但是对于 **iOS 16 以上的** 设备，你需要将 ipa 文件命名为：`原文件名@bundle-identifier.ipa`，即需要在原来的基础上加入`@bundle-identifier`，其中的 `bundle-identifier` 即 IPA 包中 `Info.plist` 的 `CFBundleIdentifier`。如：

- aszs@rn.notes.best.ipa
  推荐你使用 [ipa-renamer](https://github.com/Xhofe/ipa-renamer) 自动快速地重命名你的 IPA 文件。
- 如果你是手机用户也可以给IPA文件改名，但是你要会上述提到的格式才行，但是不提供手机改名软件请你自己解决...

:::

### Tips { lang="en" }

### Tips { lang="zh-CN" }

::: en

- **.ipa installation requires https and a valid certificate** , not just a package can be installed without a signature
  - How to change the name of the computer version

    <BiliBili bvid="BV1bT411N7tT" ratio="16:9" low-quality no-danmaku />

  - How to change the name of the IOS 16 mobile phone

    <BiliBili bvid="BV1kX4y1X7vo"/>

**Installation Demo**: Deploy **HTTPS** and **IPA files** are signed prerequisites, if **IOS16 rename by yourself** If you can’t install it yourself, please check the problem yourself

- **Installation demo environment**: IOS15.4.1 iPhone12PM, personal certificate, HTTPS

  <video src="https://r2.izyt.cc/ios/ios_ts.m3u8" controls></video>

:::
::: zh-CN

- **.ipa安装 需要 https 和 有效的证书**，不是随便一个包上传上去没签名就能安装的
- 爱思助手签名的无法使用在线安装，只能使用爱思助手安装（经群友测试）
  - 电脑版如何改名

    <BiliBili bvid="BV1bT411N7tT" ratio="16:9" low-quality no-danmaku />

  - IOS 16手机如何改名

    <BiliBili bvid="BV1kX4y1X7vo"/>

**安装演示**：部署**HTTPS**和**IPA文件**已签名前提，如果是 **IOS16自行改名** 若自己无法安装请自行排查问题所在

- **安装演示使用环境**： IOS15.4.1 iPhone12PM，个人证书，HTTPS

  <video src="https://r2.izyt.cc/ios/ios_ts.m3u8" controls></video>

:::

## 2. TrollStore install { lang="en" }

## 2. TrollStore(巨魔)安装 { lang="zh-CN" }

::: en
**Requires OpenList version ≥ 3.12.2 and above**，Devices that support the installation of TrollStore (jailbroken devices are not explained here)

For more devices, please see the table below. The content of the chart comes from [**TrollStore**](https://github.com/opa334/TrollStore)

Chart information update is uncertain, you can go to view <i class="fa-regular fa-hand-point-right" style="color: #B197FC;"></i> https://ios.cfw.guide/installing-trollstore

|          From          |           To           |                                   **arm64 (A8)**                                   |                                 arm64 (A9-A11)                                 |                             arm64e (A12-A17/M1-M2)                             |
| :--------------------: | :--------------------: | :--------------------------------------------------------------------------------: | :----------------------------------------------------------------------------: | :----------------------------------------------------------------------------: |
| 14.0 beta 1and earlier | 14.0 beta 1and earlier |                                    Unsupported                                     |                                  Unsupported                                   |                                  Unsupported                                   |
|      14.0 beta 2       |         14.8.1         |   [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx)   | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) |  [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)  |
|          15.0          |      15.5 beta 4       |    [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)    |  [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)  |  [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)  |
|          15.5          |          15.5          | [TrollInstallerMDC](https://ios.cfw.guide/installing-trollstore-trollinstallermdc) | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) |  [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)  |
|      15.6 beta 1       |      15.6 beta 3       |    [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)    |  [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)  |  [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)  |
|      15.6 beta 4       |         15.6.1         | [TrollInstallerMDC](https://ios.cfw.guide/installing-trollstore-trollinstallermdc) | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) |  [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)  |
|          15.7          |         15.7.1         | [TrollInstallerMDC](https://ios.cfw.guide/installing-trollstore-trollinstallermdc) | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) |
|         15.7.2         |         15.8.2         |       [TrollMisaka](https://ios.cfw.guide/installing-trollstore-trollmisaka)       | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) |
|      16.0 beta 1       |      16.0 beta 3       |                                   Not Applicable                                   | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) |  [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)  |
|      16.0 beta 4       |         16.6.1         |                                   Not Applicable                                   | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) |
|        16.7 RC         |        16.7 RC         |                                   Not Applicable                                   |     [TrollHelper](https://ios.cfw.guide/installing-trollstore-trollhelper)     |                                **Coming Soon**                                 |
|          16.7          |         16.7.8         |                                   Not Applicable                                   |                                  Unsupported                                   |                                  Unsupported                                   |
|      17.0 beta 1       |      17.0 beta 4       |                                   Not Applicable                                   | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) |                                **Coming Soon**                                 |
|      17.0 beta 5       |          17.0          |                                   Not Applicable                                   |     [TrollHelper](https://ios.cfw.guide/installing-trollstore-trollhelper)     |                                **Coming Soon**                                 |
|    17.0.1 and later    |    17.0.1 and later    |                                   Not Applicable                                   |                                  Unsupported                                   |                                  Unsupported                                   |

<span><a href="https://www.alipan.com/s/Z3mrsfdFY5h"><i class="fa-solid fa-party-horn fa-shake" style="color: #74C0FC;"></i> IPA Resources</a></span> :gift:

:::

::: zh-CN

**需要OpenList版本 ≥ 3.12.2 及以上**，支持安装TrollStore(巨魔)的设备（不含越狱设备）

已经支持更多设备请查看下方表格，图表内容来自 [**TrollStore**](https://github.com/opa334/TrollStore)

图表信息可能更新不及时可以前往查看 <i class="fa-regular fa-hand-point-right" style="color: #B197FC;"></i> https://ios.cfw.guide/installing-trollstore

|       开始        |       截止        |                                   **arm64 (A8)**                                   |                                 arm64 (A9-A11)                                 |                             arm64e (A12-A17/M1-M2)                             |
| :---------------: | :---------------: | :--------------------------------------------------------------------------------: | :----------------------------------------------------------------------------: | :----------------------------------------------------------------------------: |
| 14.0 beta 1及更早 | 14.0 beta 1及更早 |                                       不支持                                       |                                     不支持                                     |                                     不支持                                     |
|    14.0 beta 2    |      14.8.1       |   [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx)   | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) |  [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)  |
|       15.0        |    15.5 beta 4    |    [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)    |  [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)  |  [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)  |
|       15.5        |       15.5        | [TrollInstallerMDC](https://ios.cfw.guide/installing-trollstore-trollinstallermdc) | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) |  [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)  |
|    15.6 beta 1    |    15.6 beta 3    |    [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)    |  [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)  |  [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)  |
|    15.6 beta 4    |      15.6.1       | [TrollInstallerMDC](https://ios.cfw.guide/installing-trollstore-trollinstallermdc) | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) |  [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)  |
|       15.7        |      15.7.1       | [TrollInstallerMDC](https://ios.cfw.guide/installing-trollstore-trollinstallermdc) | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) |
|      15.7.2       |      15.8.2       |       [TrollMisaka](https://ios.cfw.guide/installing-trollstore-trollmisaka)       | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) |
|    16.0 beta 1    |    16.0 beta 3    |                                   Not Applicable                                   | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) |  [TrollHelperOTA](https://ios.cfw.guide/installing-trollstore-trollhelperota)  |
|    16.0 beta 4    |      16.6.1       |                                   Not Applicable                                   | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) |
|      16.7 RC      |      16.7 RC      |                                   Not Applicable                                   |     [TrollHelper](https://ios.cfw.guide/installing-trollstore-trollhelper)     |                                  **即将发布**                                  |
|       16.7        |      16.7.8       |                                   Not Applicable                                   |                                     不支持                                     |                                     不支持                                     |
|    17.0 beta 1    |    17.0 beta 4    |                                   Not Applicable                                   | [TrollInstallerX](https://ios.cfw.guide/installing-trollstore-trollinstallerx) |                                  **即将发布**                                  |
|    17.0 beta 5    |       17.0        |                                   Not Applicable                                   |     [TrollHelper](https://ios.cfw.guide/installing-trollstore-trollhelper)     |                                  **即将发布**                                  |
|   17.0.1及更高    |   17.0.1及更高    |                                   Not Applicable                                   |                                     不支持                                     |                                     不支持                                     |

<span><a href="https://www.alipan.com/s/Z3mrsfdFY5h"><i class="fa-solid fa-party-horn fa-shake" style="color: #74C0FC;"></i> IPA Resources</a></span> :gift:

:::

### Installation example { lang="en" }

### 安装示例 { lang="zh-CN" }

::: en

If you want to use the installation is very simple, click the **TrollStore** button to install.

![gif](https://pic.rmb.bdstatic.com/bjh/ff1e47ebc1efe5a907dbfffabf4d5f67.gif)

:::
::: zh-CN

如果你要使用安装很简单，点击 **TrollStore(巨魔)** 按钮即可安装。

![gif](https://pic.rmb.bdstatic.com/bjh/ff1e47ebc1efe5a907dbfffabf4d5f67.gif)

:::

### Other instructions { lang="en" }

### 其他说明 { lang="zh-CN" }

::: en

1. If you click the **TrollStore** button to open Apple's magnifying glass, it is because of the following reasons
   - Your `TrollStore` version number is less than version 1.3+, it is recommended to update to the latest version directly
   - Your URL scheme is not enabled. If you enable it, remember to click the first option to log out immediately **(Rebuild Now)**
     - ![TrollStore](/img/advanced/TrollStore.jpg)
2. What is the wake-up format of the TrollStore URL?
   > `apple-magnifier://install?url=<URL_to_IPA>`
3. Is there any benefit to this installation?
   - See the flow chart below for explanation

```mermaid
---
title: Is there any benefit to this installation?
---
flowchart TB
    A-->B
    subgraph A[original process]
    C[First download the application from OpenList]-->D[find the downloaded software]
    D-->E[click on the software and select share in the upper right corner]
    E-->F[find the troll icon]
    F-->G[jump into the troll software to install]
    G-->H[install and delete the software]
    end
    subgraph B[troll process]
    I[Click the OpenList troll install button and click the pop-up window prompt]-->J[enter the troll app and wait for download]
    J-->K[after downloading, click the install button]
    end
```

:::
::: zh-CN

1. 如果你点击 **TrollStore(巨魔)** 按钮后打开的是 Apple的放大镜是因为如下原因
   - 你的 `TrollStore` 版本号小于1.3+版本，建议直接更新到最新版
   - 你的使用 URL 方案没有启用，若启用后记得点击第一个选项立即注销生效 **（Rebuild Now）**
     - ![TrollStore](/img/advanced/TrollStore.jpg)
2. TrollStore URL唤醒格式是什么？
   - > `apple-magnifier://install?url=<URL_to_IPA>`
3. 这样安装有什么好处吗？
   - 解释见下面的流程图

```mermaid
---
title: 使用TrollStore安装有什么好处吗？
---
flowchart TB
    subgraph A[原生流程]
    style A fill:#bbf,stroke:#f66,stroke-width:2px,color:#fff,stroke-dasharray: 5 5
    style B fill:#ff7575,stroke:#333,stroke-width:4px
    C[1.OpenList点击下载]---|等待下载|D[2.找到软件]
    D---|右上角分享|F[3.找到巨魔图标]
    F---|点击巨魔图标|G[4.跳进巨魔软件进行安装]
    G---|安装好软件|H[5.手动删除下载的软件]
    end
    subgraph B[巨魔流程]
    I[1.点击安装按钮击弹窗提示]---|点击打开|J[2.进入巨魔应用内等待下载]
    J---|下载不占用空间|K[3.下载好然后点击安装按钮即可]
    end
    C==>I
    G==>J
    H===|使用巨魔不用手动删除|K
```

:::
