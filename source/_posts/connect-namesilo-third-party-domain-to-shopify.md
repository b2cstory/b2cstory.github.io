---
title: 将 NameSilo 购买的第三方域名绑定到 Shopify
date: 2022-05-20 11:02:22
tags: [Shopify]
categories: Shopify
cover: /img/cover/shopify.png
top_img: /img/cover/shopify.png
description: 本文主要为大家介绍如何将我们在 NameSilo 购买的第三方域名绑定至 Shopify 独立站。
---

在本文开始之前，我们先以本站的域名为例简单为大家介绍一下主域名和二级域名的基本概念：

- `b2cstory.myshopify.com`：这是我们注册 Shopify 商店后由 Shopify 分配给我们的二级域名，所有权是属于 Shopify 的。
- `b2cstory.com`：这是我们在 [NameSilo](https://www.namesilo.com/?rid=509a222yb) 购买的主域名，所有权是属于我们自己的。
- `shopify.b2cstory.com`：这是我们的其中一个二级域名，所有权也是属于我们自己的。

其中主域名是只有一个的，而在该主域名下，可以添加多个二级域名。

一般来说，为了推广我们的独立站，为用户树立一个良好的品牌形象，我们都会去购买一个品牌相关的主域名。在 Shopify 的后台就可以完成主域名的购买，价格一般在 14 美元 / 年；而我们在 [NameSilo](https://www.namesilo.com/?rid=509a222yb) 购买的主域名则稍微便宜一点，价格为 9.95 美元 / 年。如果你是在 Shopify 后台购买的主域名，无需进行额外的配置就可以将主域名绑定到我们的独立站；如果你是在第三方域名提供商购买的主域名，则需要进行相应的设置才能使我们购买的主域名绑定到 Shopify 商店，使用户可以通过我们的主域名进行访问。

本文就以从 [NameSilo](https://www.namesilo.com/?rid=509a222yb) 购买的域名为例，为大家介绍一下如何将第三方的域名绑定到 Shopify 独立站。

## 一、更改 NameSilo 中的 DNS 记录

打开 [NameSilo](https://www.namesilo.com/?rid=509a222yb) 的网站后，登录我们的账户，然后点击顶部菜单的 **My Account** 进入账户管理界面。

![点击 My Account 打开账户管理](/connect-namesilo-third-party-domain-to-shopify/namesilo-open-my-account.jpg)

接着在 Account Domains 右侧，点击那个【**1**】(这里我们只购买了一个域名，所以显示的是 1，如果你购买的域名不止一个，则会显示对应的数量)。

![点击管理域名](/connect-namesilo-third-party-domain-to-shopify/namesilo-account-home-page.jpg)

在域名管理页面，找到我们的域名，然后点击右侧的【**地球图标**】，进入 DNS 管理界面。

![点击 DNS 管理图标](/connect-namesilo-third-party-domain-to-shopify/namesilo-domain-manager.jpg)

在 DNS 管理界面，[NameSilo](https://www.namesilo.com/?rid=509a222yb) 默认是有 4 条 DNS 记录的，我们只需要保留一条 **A** 记录和一条 **CNAME** 记录然后对二者进行修改即可，另外的记录可以点击右侧的 ❌ 号直接删除掉。

点击 EDIT 的图标，分别对 **A** 记录和 **CNAME** 记录作如下修改，其中 **TTL** 我们保持默认的值即可，完成后结果如下图所示。

- 将 **A** 记录指向 Shopify IP 地址 `23.227.38.65`。
- 将名称为 **www** 的 **CNAME** 记录指向 `shops.myshopify.com`。

![修改后的结果](/connect-namesilo-third-party-domain-to-shopify/namesilo-manage-dns.png)

## 二、将第三方域名连接到 Shopify

在 Shopify 后台中，点击左下角的【**设置**】，在左侧菜单栏选择【**域名**】，然后点击【**连接现有域名**】按钮。

![连接现有域名](/connect-namesilo-third-party-domain-to-shopify/shopify-domain-settings.png)

输入我们购买的主域名，如 `b2cstory.com`，然后点击【**下一步**】按钮。

![输入第三方域名](/connect-namesilo-third-party-domain-to-shopify/shopify-connect-existing-domain.png)

接着我们点击【**验证连接**】按钮查看第三方域名是否绑定成功即可。如果显示【**域名连接未完成**】也不用担心，因为域名验证可能最多需要 48 小时才能完成。我们可以耐心等待一段时间再【**验证连接**】。

![验证连接](/connect-namesilo-third-party-domain-to-shopify/shopify-3rd-party-domain-verify-connection.png)

经过验证后，会提示我们 Your domain, xxx.com was successfully connected，这样我们在 [NameSilo](https://www.namesilo.com/?rid=509a222yb) 购买的域名就成功的绑定到 Shopify 了。

![绑定成功提示](/connect-namesilo-third-party-domain-to-shopify/shopify-domain-connect-successfully.png)

最后，我们在浏览器输入自己的主域名，看看能否成功打开即可。
