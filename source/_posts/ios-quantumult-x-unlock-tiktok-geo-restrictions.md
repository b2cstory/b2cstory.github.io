---
title: iOS 使用 Quantumult X 免拔卡解锁 TikTok 区域限制
date: 2021-06-16 03:33:49
tags: [TikTok]
categories: TikTok
cover: /ios-quantumult-x-unlock-tiktok-geo-restrictions/tiktok-banner.png
top_img: /ios-quantumult-x-unlock-tiktok-geo-restrictions/tiktok-banner.png
description: 本文主要介绍了如何在iPhone上使用Quantumult X免拔卡解锁TikTok的区域限制。
---

## 一、准备工作

1. 一台可以正常使用的 iPhone；
2. 一个美区 Apple ID，可参考《[如何注册美区 Apple ID 下载国际版抖音 TikTok](https://b2cstory.com/sign-up-us-apple-id-to-download-tiktok/)》一文；
3. 通过充值或礼品卡购买并下载 [Quantumult X](https://apps.apple.com/us/app/quantumult-x/id1443988620) (售价 7.99 美元)；
4. 一个可以正常使用的节点 (由于 TikTok 已退出香港市场，故香港节点无法使用)，个人推荐在 [Just My Socks](https://justmysocks.net/members/aff.php?aff=16410) 进行购买，可以使用支付宝付款；
5. 对手机进行相关设置伪装海外环境，可参考《[iPhone 如何伪装真实海外环境进行 TikTok 账号运营](https://b2cstory.com/simulate-overseas-environment-with-iphone/)》一文。

## 二、生成信任证书

1. 打开 Quantumult X 主界面，点击右下角的圆形按钮，找到 MinM 模块，点击生成密钥及证书 (Generate CA)，提示生成成功，点击安装证书后会跳转到 Safari，提示需要下载一个配置描述文件，我们点击允许即可；
2. 进入 iOS 系统设置 (Settings) >> 通用 (General) >> 描述文件 (Profile) >> 已下载的描述文件 >> 选中并安装，输入密码后即可完成描述文件安装；
3. 进入 iOS 系统设置 (Settings) >> 通用 (General) >> 关于本机 (About) >> 证书信任设置 (Certificate Trust Settings) >> 启用刚刚安装的证书即可。

## 三、编辑 Quantumult X 配置文件

### 方法一

1. 进入 Quantumult X，点击右下角的圆形按钮，下拉至最后，在配置文件 (Profile) 模块的下面点击编辑 (Edit)，然后找到 `[rewrite_remote]` 并在其下方添加以下对应国家的复写，以美国为例如下图所示。

![在 [rewrite_remote] 下添加对应国家的复写](/ios-quantumult-x-unlock-tiktok-geo-restrictions/rewrite-remote-codes.jpg)

**日本**

```
https://raw.githubusercontent.com/Semporia/TikTok-Unlock/master/Quantumult%20X/TikTok-JP.conf, tag=TikTok, update-interval=86400, opt-parser=false, enabled=true
```

**台湾**

```
https://raw.githubusercontent.com/Semporia/TikTok-Unlock/master/Quantumult%20X/TikTok-TW.conf, tag=TikTok, update-interval=86400, opt-parser=false, enabled=true
```

**韩国**

```
https://raw.githubusercontent.com/Semporia/TikTok-Unlock/master/Quantumult%20X/TikTok-KR.conf, tag=TikTok, update-interval=86400, opt-parser=false, enabled=true
```

**美国**

```
https://raw.githubusercontent.com/Semporia/TikTok-Unlock/master/Quantumult%20X/TikTok-US.conf, tag=TikTok, update-interval=86400, opt-parser=false, enabled=true
```

2. 找到 `[filter_remote]` 并在其下方粘贴以下相应代码，然后点击右上角保存。

```
https://raw.githubusercontent.com/Semporia/Quantumult-X/master/Filter/TikTok.list, tag=TikTok, force-policy=TikTok, update-interval=86400, opt-parser=false, enabled=true
```

### 方法二

1. 进入 Quantumult X，点击右下角的圆形按钮，下拉至最后，在配置文件 (Profile) 模块的下面点击编辑 (Edit)，如下图所示。

![编辑 Quantumult X 配置文件](/ios-quantumult-x-unlock-tiktok-geo-restrictions/quantumult-x-settings.png)

2. 打开配置文件后，找到 `[rewrite_local]`，并在其下方粘贴以下相应代码，然后点击右上角保存。如果你使用的是香港手机号码，则需要将第二行中的 `CN` 修改为 `HK`。

```
#TikTok 解锁直播区域限制
(?<=_region=)CN(?=&) url 307 US
(?<=&mcc_mnc=)4 url 307 2
^(https?:\/\/(tnc|dm)[\w-]+\.\w+\.com\/.+)(\?)(.+) url 302  $1$3
(?<=\d\/\?\w{7}_\w{4}=)1[6-9]..(?=.?.?&) url 307 17
```

3. 找到 `[mitm]` 并在其下方粘贴以下相应代码，然后点击右上角保存。

```
hostname = *.tiktokv.com, *.byteoversea.com, *.tik-tokapi.com
```

4. 找到 `[filter_remote]` 并在其下方粘贴以下相应代码，然后点击右上角保存。

```
https://raw.githubusercontent.com/Semporia/Quantumult-X/master/Filter/TikTok.list, tag=TikTok, force-policy=TikTok, update-interval=86400, opt-parser=false, enabled=true
```

5. 换区方法：在 `[rewrite_local]` 中的 US 可以根据自己的需要替换成对应国家的 2 位大些英文简称。更加详细的 TikTok 国家/地区代码请参考《[TikTok 国家/地区代码](https://b2cstory.com/tiktok-country-code/)》。
- 日本：JP
  
- 韩国：KR
  
- 英国：UK
  
- 美国：US
  
- 台湾：TW

最终如下图所示：

![将三段代码粘贴到对应的位置](/ios-quantumult-x-unlock-tiktok-geo-restrictions/quantumult-x-codes.jpg)

最后，回到 Quantumult X 的首页，下滑至最下方找到 TikTok 的策略，点击后选择 PROXY 连接即可。

## 四、开启 Rewrite 和 MitM

继续返回 Quantumult X 主界面，点击右下角的圆形按钮。找到 Rewrite 模块和 MitM 模块，将两个模块都启用即可，如下图所示。

![开启 Rewrite 和 MitM](/ios-quantumult-x-unlock-tiktok-geo-restrictions/open-rewrite-and-mitm.jpeg)

接下来我们就可以免拔卡解锁 TikTok 区域限制，随意使用了。

最后建议不要对 TikTok 的版本进行更新，避免更新后代码失效无法使用。

------

**注：**本文参考了[毒奶的博文](https://limbopro.xyz/archives/11773.html)，并依据 [CC BY-NC-SA 4.0 授权协议](https://creativecommons.org/licenses/by-nc/4.0/deed.zh-Hans)针对外贸从业者进行了简化。
