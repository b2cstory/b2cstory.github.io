---
title: Shopify Brooklyn 主题固定菜单栏并避免手机端遮挡产品图片
date: 2021-04-04 03:04:52
updated: 2021-04-04 03:04:52
tags: [Shopify, Shopify Theme]
categories: Shopify
cover: /shopify-brooklyn-theme-sticky-header/shopify-brooklyn-theme-cover.jpeg
top_img: /shopify-brooklyn-theme-sticky-header/shopify-brooklyn-theme-cover.jpeg
description: 本文为大家介绍一下如何为 Shopify Brooklyn 主题设置固定菜单栏，并且如何避免手机端出现产品图片被遮挡的问题。
---

本文为大家介绍一下如何为 Shopify Brooklyn 主题设置固定菜单栏，并且如何避免手机端出现产品图片被遮挡的问题。

Brooklyn 主题是由 Shopify 官方推出的一款免费主题。对于刚刚进入独立站这个行业，资金还不是很充裕的卖家来说，Brooklyn 这款免费的主题是一个极为不错的选择。当然，相比 [Turbo Portland 主题](https://outofthesandbox.com/products/turbo-theme-portland?rfsn=4714227.94d985b&utm_source=refersion&utm_medium=affiliate&utm_campaign=4714227.94d985b)或者其他一些更加专业性的主题来说，Brooklyn 在可自定义程度上还是有些不足。如果在功能方面有更高的要求，可能就需要通过自定义代码或是安装 App 的形式来实现。

本着能自己用代码解决就绝不多装一个 App 的原则（避免拖慢网站速度），接下来就为大家介绍如何通过自定义代码，将 Brooklyn 主题的主菜单设置为固定菜单，即向下滑动页面的时候主菜单始终位于顶部。另外，目前网络上虽然也有类似的教程，但大多设置完后会在手机端出现 bug，即在手机端查看产品页面的时候，产品图片会被固定的主菜单遮挡一部分。而对于独立站卖家来说，手机端的界面是远比桌面端要重要的，绝大多数卖家的手机端流量都会超过 70%。所以，本文就提供一种方法将手机端的这个 bug 也一并解决。

## 一、备份主题

**在开始之前，请一定要记住先备份一下主题！**

## 二、添加 CSS 代码设置主菜单的样式

首先，我们要通过 **Online Store >> Theme >> Customize** 进入主题自定义页面，在 Home Page 的模版中选择 Header，并将 Enable Transparent Header on the Homepage 取消勾选，以免与将要添加的代码冲突。

![取消勾选 Enable Transparent Header on the Homepage](/shopify-brooklyn-theme-sticky-header/brooklyn-disable-transparent-header-on-the-homepage.png)

然后我们来到 Shopify 店铺的后台，通过 **Online Store >> Theme >> Actions >> Edit Code** 进入 Brooklyn 主题的代码编辑页面。在搜索栏搜索 **theme.scss.liquid** 并打开 **theme.scss.liquid** 这个代码文件。

![搜索 theme.scss.liquid 代码文件并打开](/shopify-brooklyn-theme-sticky-header/shopify-brooklyn-theme-search-css-file.png)

接下来，我们将页面滑倒底部，复制下面提供的代码，然后粘贴到最后的位置并点击右上角绿色的 Save 按钮保存，如下图所示。这一部分主要是设置了主菜单的样式，分别是将主菜单的背景设置为白色，并且分别在顶部和底部加上两条半透明的分割线。

```css
/* Sticky Header for Brooklyn Theme | b2cstory.com */
 .site-header {
 padding-top: 0;
 background: #ffffff;
 border-bottom: 1px solid rgba(200,200,200,.5);
 border-top: 1px solid rgba(200,200,200,.5);
 }
```

![将以上代码粘贴至 theme.scss.liquid 最后](/shopify-brooklyn-theme-sticky-header/shopify-brooklyn-theme-add-header-style.png)

## 三、添加 JS 代码使主菜单固定

第二步，我们要添加 JS 代码使主菜单固定。在 Brooklyn 主题的代码编辑页面搜索 **theme.js.liquid** 并打开 **theme.js.liquid** 这个代码文件。依旧是将页面滑倒底部，复制下面提供的代码，然后粘贴到最后的位置并点击右上角绿色的 Save 按钮保存即可，如下图所示。

```javascript
// Sticky Header for Brooklyn Theme | b2cstory.com
var oTop = $(".site-header").offset().top;
 var martop = $('.site-header').outerHeight();
 var sTop = 0;
 $(window).scroll(function () {
     sTop = $(this).scrollTop();
     if (sTop >= oTop) {
         $(".site-header").css({ "position": "fixed", "top": "0",'width':'100%' });
         $(".main-content").css({ "margin-top": martop });
     } else {
         $(".site-header").css({ "position": "static" });
         $(".main-content").css({ "margin-top": "0" });
     }
 })
```

![将以上代码粘贴至 theme.js.liquid 最后](/shopify-brooklyn-theme-sticky-header/shopify-brooklyn-theme-add-sticky-header-js-code.png)

最后，我们可以拿出手机来查看一下效果了。如下图所示，滑动的时候可以确保顶部菜单是固定的，而且产品页的产品图片也并没有被主菜单所遮挡，完美地达到了我们预期的效果。

![Brooklyn 主题 Sticky Header 手机端效果](/shopify-brooklyn-theme-sticky-header/shopify-brooklyn-theme-sticky-header-in-mobile.png)

由于 Shopify 官方也会不定期维护 Brooklyn 主题并更新代码，所以本教程并不能保证永久有效，至少在本文发出时，这个方法还是有效可行的。
