# 相芯美颜插件快速开始

> 本文档主要介绍如何快速跑通 <mark>相芯美颜插件</mark> Flutter 示例工程
>
> 其他语言版本: [**English**](README.md)
---

## 1. 环境准备

- <mark>最低兼容 Android 5.0</mark>（SDK API Level 21）
- Flutter SDK 2.10及以上版本。
- Android 5.0 及以上的真机设备。

---

## 2. 运行示例

##### 2.1 获取声网 App ID -------- [声网Agora - 文档中心 - 如何获取 App ID](https://docs.agora.io/cn/Agora%20Platform/get_appid_token?platform=All%20Platforms#%E8%8E%B7%E5%8F%96-app-id)

> - 点击创建应用
>
>   ![xxx](https://accktvpic.oss-cn-beijing.aliyuncs.com/pic/github_readme/create_app_1.jpg)
>
> - 选择你要创建的应用类型
>
>   ![xxx](https://accktvpic.oss-cn-beijing.aliyuncs.com/pic/github_readme/create_app_2.jpg)
>
> - 得到 App ID 与 App 证书
>
>   ![xxx](https://accktvpic.oss-cn-beijing.aliyuncs.com/pic/github_readme/get_app_id.jpg)

##### 2.2 在声网控制台 [购买和激活](https://docs.agora.io/cn/extension_customer/get_extension?platform=All%20Platforms) 相芯美颜道具高级版插件，点击**联系我们**获取专属的证书文件

- 申请时请提供绑定 License 的包名, 并将项目 [**android/app/build.gradle**](android/app/build.gradle) 文件中的applicaitionId 改为您自己 License 绑定的包名

![xxx](https://accktvpic.oss-cn-beijing.aliyuncs.com/pic/github_readme/market-place/FaceUnity/FaceUnity_flutter_1.png)

##### 2.3 在项目的 [**lib/main.dart**](lib/main.dart) 里填写需要的声网 App ID:

![xxx](https://web-cdn.agora.io/docs-files/1681456048918)


##### 2.4 将相芯美颜需要的资源文件拷贝到项目的 [**Resource/**](Resource/) 目录下

* [点击此处下载demo需要的资源文件包](https://download.agora.io/marketplace/release/FaceUnity_v8.4.1_Resources.zip)

![xxx](https://web-cdn.agora.io/docs-files/1673335775613)

##### 2.5 将相芯美颜ios authpack.h 内容拷贝到[lib/authpack.dart](lib/authpack.dart) `gAuthPackage`中。

![xxx](https://accktvpic.oss-cn-beijing.aliyuncs.com/pic/github_readme/market-place/FaceUnity/FaceUnity_flutter_2.png)

##### 2.6 下载插件 android-release.aar 文件, 并拷贝到项目 [**android/libs/**](android/libs/) 目录下

* [点击此处下载demo需要的插件aar](https://download.agora.io/marketplace/release/Agora_Marketplace_FaceUnity_v8.4.1_Extension_for_Android_v4.1.1.zip)



<img src="https://web-cdn.agora.io/docs-files/1673335651833" alt="xxx" style="zoom:50%;" />

##### 2.7 用你熟悉的IDE(Android Studio 或者 VS Code)打开项目, 连接一台 Android 真机（非模拟器），运行项目

---

## 3. 项目介绍

### 3.1 概述

> 该项目展示了如何通过简单的 API 调用快速集成声网云市场相芯美颜插件

### 3.2 项目文件结构简介

```
├── android
│   |
│   └── libs //放置插件 aar
│   └── build.gradle //Gradle 构建脚本
├── .gitignore
├── ios
|__ Resource // 美颜资源文件
```

---

## 4. FAQ

### 如何获取声网 APPID

> 声网 APPID 申请：[声网Agora - 文档中心 - 如何获取 App ID](https://docs.agora.io/cn/Agora%20Platform/get_appid_token?platform=All%20Platforms#%E8%8E%B7%E5%8F%96-app-id)

### 程序运行后，没有美颜效果
> 通常有以下几个原因：

> 1、插件动态库没有保存在正确位置，或者没有导入；
> 2、相芯资源包中的文件没有保存在正确位置，或者缺少部分文件；
> 3、证书文件与 app 包名不一致，导致鉴权失败。

### 想了解声网的其他云市场插件

> 声网云市场官网入口: https://www.shengwang.cn/cn/marketplace/

### 集成遇到困难，该如何联系声网获取协助

> 方案1：如果您已经在使用声网服务或者在对接中，可以直接联系对接的销售或服务；
>
> 方案2：发送邮件给 [support@agora.io](mailto:support@agora.io) 咨询

---