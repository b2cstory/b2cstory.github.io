---
title: iOS 使用 Shadowrocket 免拔卡解锁 TikTok 区域限制
date: 2021-06-16 03:34:59
updated: 2021-06-16 03:34:59
tags: [TikTok]
categories: TikTok
cover: /ios-shadowrocket-unlock-tiktok-geo-restrictions/tiktok-banner.png
top_img: /ios-quantumult-x-unlock-tiktok-geo-restrictions/tiktok-banner.png
description: 本文主要介绍了如何在iPhone上使用Shadowrocket免拔卡解锁TikTok的区域限制。
---

## 一、准备工作

1. 一台可以正常使用的 iPhone；
2. 一个美区 Apple ID，可参考《[如何注册美区 Apple ID 下载国际版抖音 TikTok](https://b2cstory.com/sign-up-us-apple-id-to-download-tiktok/)》一文；
3. 通过充值或礼品卡购买并下载 [Shadowrocket](https://apps.apple.com/us/app/shadowrocket/id932747118) (售价 2.99 美元)；
4. 一个可以正常使用的节点 (由于 TikTok 已退出香港市场，故香港节点无法使用)，个人推荐在 [Just My Socks](https://justmysocks.net/members/aff.php?aff=16410) 进行购买，可以使用支付宝付款；
5. 对手机进行相关设置伪装海外环境，可参考《[iPhone 如何伪装真实海外环境进行 TikTok 账号运营](https://b2cstory.com/simulate-overseas-environment-with-iphone/)》一文。

## 二、生成证书文件

1. 打开 Shadowrocket，点击配置并选择默认的配置文件 default.conf，依次选择编辑配置 (Edit Config) >> 开启 HTTPS 解密 (HTTPS Decryption) >> 生成新的 CA证书 (Generate A New CA Certificate) >> 安装证书 (Install CA Certificate to System) >> 允许；
2. 进入 iOS 系统设置 (Settings) >> 通用 (General) >> 描述文件 (Profile) >> 选中已下载的 Shadowrocket 描述文件并安装 >> 输入锁屏密码 >> 点击右上角安装；
3. 进入 iOS 系统设置 (Settings)，依次点击通用 (General) >> 关于本机 (About) >> 下拉到最后找到证书信任设置 (Certificate Trust Settings) >> 启用生成的 Shadowrocket 证书 >> 弹出警告框 >> 继续。

## 三、编辑配置文件

1. 打开 Shadowrocket，选择配置 (Config)，点击默认的配置文件 default.conf，然后点击编辑纯文本 (Edit Plain Text)，打开文本编辑页面后下拉找到 `[URL Rewrite]` 和 `[MITM]` 两部分；
2. 在 `[URL Rewrite]` 和 `[MITM]` 之后分别添加以下两段代码：

```
(?<=_region=)CN(?=&) US 307
(?<=&mcc_mnc=)4 2 307
^(https?:\/\/(tnc|dm)[\w-]+\.\w+\.com\/.+)(\?)(.+) $1$3 302
(?<=\d\/\?\w{7}_\w{4}=)1[6-9]..(?=.?.?&) 17 307
```

```
hostname = *.tiktokv.com, *.byteoversea.com, *.tik-tokapi.com
```

其中 `[URL Rewrite]` 第一行中的 US 可以根据自己的需要替换成对应国家的代码，比如想刷日区的 TikTok 就将 US 改成 JP 即可。更加详细的 TikTok 国家/地区代码请参考《[TikTok 国家/地区代码](https://b2cstory.com/tiktok-country-code/)》。

最终效果如下图所示：

![将两段代码添加到对应的位置](/ios-shadowrocket-unlock-tiktok-geo-restrictions/shadowrocket-url-rewrite-and-mitm.jpeg)

接下来我们就可以免拔卡解锁 TikTok 区域限制，随意使用了。

最后建议不要对 TikTok 的版本进行更新，避免更新后代码失效无法使用。

---

**注：**本文参考了[毒奶的博文](https://limbopro.xyz/archives/Shadowrocket-Tiktok.html)，并依据 [CC BY-NC-SA 3.0 授权协议](https://creativecommons.org/licenses/by-nc-sa/3.0/hk/deed.zh)针对外贸从业者进行了修改。
