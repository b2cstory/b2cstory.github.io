---
title: 为 Shopify 店铺创建 Track Your Order 页面
date: 2021-03-31 02:30:22
updated: 2021-03-31 02:30:22
tags: [Shopify]
categories: Shopify
cover: /shopify-track-your-order-page/shopify-track-your-order-page-cover.png
top_img: /shopify-track-your-order-page/shopify-track-your-order-page-cover.png
description: 本文为大家介绍如何通过外部调用 17TRACK 为自己的 Shopify 店铺创建 Track Your Order 页面。
---

本文为大家介绍如何通过外部调用 17TRACK 为自己的 Shopify 店铺创建 Track Your Order 页面。

虽然 Shopify App Store 中有很多 App 可以实现这个功能，但是大家都知道多装一个 App，网站的速度就被拖慢一点。本着能不装 App 就不装的原则，我们可以通过一段简单的代码就能轻松的在自己的 Shopify 店铺上创建一个 Track Your Order 页面。此外，将 Track Your Order 页面放在我们网站的主菜单或是底部，也可以增强用户对我们店铺的信任感。

接下来，我们就以 [Turbo 主题](https://outofthesandbox.com/products/turbo-theme-portland?rfsn=4714227.94d985b&utm_source=refersion&utm_medium=affiliate&utm_campaign=4714227.94d985b)为例，给大家示范一下如何操作以及最终可以实现的效果。

首先，我们来到 Shopify 店铺的后台，在 **Online Store >> Pages** 中添加一个新的页面。然后点击 Show HTML 的图标进入代码编辑模式，将下边给出的代码复制进去，保存后即可预览页面查看效果。

![点击 Show HTML 图标进入代码编辑模式并粘贴以下代码](/shopify-track-your-order-page/shopify-add-track-your-order-page.png)

```html
<div align="center" style="margin-top:10px; margin-bottom:20px">
<input class="Form__Input" type="text" placeholder="Enter your number" id="YQNum" maxlength="50" style="width:100%; height:57px">
<input class="Button" style="background:#000; border-radius:0; width:100%; height:50px; margin-left:0px; color:#fff" type="button" value="TRACK" onclick="doTrack()">
<div id="YQContainer"></div>
<script type="text/javascript" src="//www.17track.net/externalcall.js"></script>
<script type="text/javascript">
function doTrack() {
    var num = document.getElementById("YQNum").value;
    if(num===""){
        alert("Enter your number.");
        return;
    }
    YQV5.trackSingle({
        YQ_ContainerId:"YQContainer",
        YQ_Height:560,
        YQ_Fc:"0",
        YQ_Lang:"en", YQ_Num:num
    });
}
</script>
</div>
```

接下来，我们可以在下面继续补充一些自己的配送政策或者物流相关的 FAQ 等，使 Track Your Order 页面更加完善。最终实现的效果如下图所示。

![Turbo Portland 主题下的 Track Your Order 页面效果](/shopify-track-your-order-page/rendering-of-shopify-track-your-order-page.png)
