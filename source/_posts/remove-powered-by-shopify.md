---
title: 如何移除 Shopify 商店底部的 “Powered by Shopify”
date: 2022-04-25 08:16:55
tags: [Shopify]
categories: Shopify
cover: /create-a-shopify-store/shopify-banner.png
top_img: /create-a-shopify-store/shopify-banner.png
description: 本文为大家介绍了如何通过 Shopify 模版编辑语言页面或是通过 Shopify 模版编辑代码页面移除 Shopify 商店前端的“Powered by Shopify”。
---

{% btn 'https://zh.shopify.com/',立即注册 Shopify 商店享受 14 天免费试用,far fa-hand-point-right,orange block center larger %}

在我们的 Shopify 商店注册完成后，会发现商店每个页面的底部都会显示 “Powered by Shopify”，这会让访问我们商店的人知道我们的在线商店是通过 Shopify 这个平台进行搭建的。对很对卖家而言，“Powered by Shopify” 并不是我们所必须的，我们可能不想让我们的用户或是竞争对手知道我们的在线商店是通过 Shopify 搭建的。接下来，我们就为大家介绍几种方法，来把 Shopify 在线商店底部的 “Powered by Shopify” 移除掉。

## 方法一：通过 Shopify 模版编辑语言页面移除

1. 登录到 Shopify 商店的后台后，依次点击**在线商店 > 模版 > 编辑 > 编辑 > 编辑语言**。

![编辑语言](/remove-powered-by-shopify/shopify-online-store-edit-languages.jpg)

2. 在**搜索翻译**框中输入 `powered`，可以看到在 **Links** 和 **Password page** 中的内容就是商店前端显示的“Powered by Shopify”。

![搜索 powered](/remove-powered-by-shopify/shopify-edit-languages-search-powered.jpg)

3. 在 **Powered by Shopify** 框中，使用键盘上的空格键来输入一个空格，即可移除商店前端显示的“Powered by Shopify”。

4. 在 **Powered by Shopify HTML** 框用空格替代原来的内容，则会移除我们商店**即将开业**页面上显示的“Powered by Shopify”。

5. 如果我们想让原本显示“Powered by Shopify”的地方显示我们的自定义内容，则用我们想输入的内容来替换掉刚才输入的空格并保存即可，例如我们想显示“Welcome to B2C Story!”，则文本框中输入的内容和商店前端展示的内容分别如下图所示。

![输入 Welcome to B2C Story!](/remove-powered-by-shopify/shopify-edit-languages-weolcom-to-b2c-story.jpg)

![商店底部显示我们的自定义内容](/remove-powered-by-shopify/store-home-page-welcom-to-b2c-story.jpg)

## 方法二：通过 Shopify 模版编辑代码页面移除

1. 登录到 Shopify 商店的后台，依次点击**在线商店 — 模版 — 编辑 — 编辑代码**，打开我们所安装主题的代码管理页面。

![编辑模版代码](/remove-powered-by-shopify/shopify-online-store-edit-code.jpg)

2. 在搜索框中输入 `footer.liquid` 并点击该文件打开，可以在右侧看到该文件下所包含的代码。

![搜索并打开 footer.liquid 文件](/remove-powered-by-shopify/shopify-edit-footer-code.jpg)

3. 在右侧代码部分通过快捷键 Ctrl + F 或者 command + F 打开搜索框，并输入 powered 进行搜索，我们只需要把 `{{ powered_by_link }}` 所在的这一行代码删除即可移除掉商店前端显示的“Powered by Shopify”。

![搜索 powered](/remove-powered-by-shopify/shopify-edit-code-search-powered.jpg)

4. 如果我们想要将“Powered by Shopify”替换成自定义内容，则只需用我们的自定义内容替换掉 `{{ powered_by_link }}` ，并将其所在行的其他代码予以保留，如下面代码所示。

```html
<small class="copyright__content">Welcome to B2C Story!</small>
```

5. 最后，需要注意的是，对于不同的主题，此处显示的代码可能会略有不同，如果你担心自己修改会出错而导致商店前端无法正常显示，建议在 [Fiverr](https://www.fiverr.com/) 这类自由职业者平台上找一个代码专家进行修改。不过在进行任何代码的改动之前，我们都要记得备份一下主题。
