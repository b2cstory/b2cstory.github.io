---
title: 通过自定义代码为 Shopify 产品页添加预计交付日期
date: 2022-05-20 12:56:49
tags: [Shopify]
categories: Shopify
cover: /img/cover/shopify.png
top_img: /img/cover/shopify.png
description: 本文为大家介绍如何通过自定义代码的形式，无需安装插件，在 Shopify 的产品页显示预计到货日期。
---

本教程的目标是在 Shopify 的产品页显示一个预计送达日期的范围，如 6 到 12 天。系统会自动计算出大概的送达日期范围，不过购买当天和周六周日是不会被计入其中的。

另外，本教程所使用的主题是默认的 **Dawn** 主题，不过如果你使用的 Shopify 主题支持 Online Store 2.0，那么实现过程应该是一样的。具体的实现效果如下图所示。

{% note warning flat %}
如果你想打开网页看看实际效果，可以访问 https://shopify.b2cstory.com/ 并输入密码 `b2cstory` 后打开产品自行查看。
{% endnote %}

![预计送达日期在产品页的实际效果](/display-the-estimated-delivery-date-on-shopify-product-page/final-result-of-estimated-delivery-date.jpg)

首先打开 Shopify 独立站的后台，通过【**在线商店 > 模版 > 编辑 > 自定义**】进入主题编辑页面。

![编辑 Shopify 主题](/display-the-estimated-delivery-date-on-shopify-product-page/shopify-customize-theme.jpg)

中间的下拉选项框默认显示的是主页，我们在下拉菜单选择【**产品**】，然后点击【**默认产品**】。

![选择默认产品](/display-the-estimated-delivery-date-on-shopify-product-page/shopify-edit-product-template.jpg)

接着在左侧菜单的产品信息下方点击【**添加块**】，选择【**自定义 liquid**】，然后将其拖动到我们想要展示的位置，这里我们是拖动了【**自定义 liquid**】使其在价格下方显示。

![添加自定义 liquid 块](/display-the-estimated-delivery-date-on-shopify-product-page/shopify-theme-add-custom-liquid.png)

复制下方代码并粘贴到【**自定义 liquid**】文本框中，然后点击右上角的【**保存**】即可。

![粘贴代码到自定义 liquid 并保存](/display-the-estimated-delivery-date-on-shopify-product-page/paste-codes-and-save.jpg)

```html
<!-- Estimated Delivery Date | b2cstory.com -->
<style>
.estimated-delivery-date {
	margin: 10px 0 10px 0;
	letter-spacing: 0.01em;
	text-transform: uppercase;
}
.estimated-delivery-date p {
	font-size: 11px;
	line-height: 22px;
	color: #333;
}
.estimated-delivery-date p span {
	color: #4ca868;
}
</style>
<div class="estimated-delivery-date">
	<p>
		<img src="https://cdn.shopify.com/s/files/1/0584/1200/7563/files/refund.png?v=1653029463" style="height: 25px; float: left; margin-right: 10px; padding-bottom: 4px;">
            Free returns <span>under 30 days</span>
    </p>
    <p>
        <img src="https://cdn.shopify.com/s/files/1/0584/1200/7563/files/package.png?v=1653029463" style="height: 25px; float: left; margin-right: 10px; padding-bottom: 3px;">
            Only available <span>online</span>
    </p>
    <p>
        <img src="https://cdn.shopify.com/s/files/1/0584/1200/7563/files/truck.png?v=1653029463" style="height: 25px; float: left; margin-right: 10px; padding-bottom: 3px;">
            Delivery estimated within <span id="fromDate">20/11</span> and <span id="toDate">29/11</span>
    </p>
</div>
<script src="//cdnjs.cloudflare.com/ajax/libs/datejs/1.0/date.min.js" type="text/javascript"></script>
<script>
(function () {
    if (document.getElementById('fromDate')) {
        var dateStart = 6;
        var dateEnd = 12;
        var fromDate = Date.today().addDays(dateStart);
        if (fromDate.is().saturday() || fromDate.is().sunday()) {
            fromDate = fromDate.next().monday();
        }
        var toDate = Date.today().addDays(dateEnd);
        if (toDate.is().saturday() || toDate.is().sunday()) {
            toDate = toDate.next().monday();
        }
        document.getElementById('fromDate').innerHTML = fromDate.toString('dd/MM');
        document.getElementById('toDate').innerHTML = toDate.toString('dd/MM');
    }
})();
</script>
<!-- Estimated Delivery Date | b2cstory.com -->
```

这里我们总共添加了三行，分别是退货信息、仅在网上销售、预计送达日期。

- 如果你想将绿色的字体修改为其他颜色，则需要将代码第 4 行中的 `#4ca868` 修改为你需要的颜色代码。
- 如果你不想全大写显示，则将第 6 行的代码删除即可。
- 如果你需要替换每一行前面的图标，则需要将代码第 19 行、第 23 行、第 27 行中的图片链接替换为你自己的图标链接。
- 如果你想修改文字内容，需要编辑代码的第 20 行、第 24 行和第 28 行。

- 如果你想修改预计送达日期的范围，则需要将代码第 35 行和第 36 行中的 6 和 12 修改为你的产品的预计送达日期范围。

如果我们只想显示预计到货日期，则复制粘贴下方的代码到【**自定义 liquid**】文本框中即可。

```html
<!-- Estimated Delivery Date | b2cstory.com -->
<style>
.estimated-delivery-date {
    margin: 10px 0 10px 0;
	letter-spacing: 0.01em;
	text-transform: uppercase;
}
.estimated-delivery-date p {
	color: #333;
	font-size: 11px;
	line-height: 22px;
	color: #333;
}
.estimated-delivery-date p span {
	color: #4ca868;
}
</style>
<div class="estimated-delivery-date">
    <p>
        <img src="https://cdn.shopify.com/s/files/1/0584/1200/7563/files/truck.png?v=1653029463" style="height: 25px; float: left; margin-right: 10px; padding-bottom: 3px;">
            Delivery estimated within <span id="fromDate">20/11</span> and <span id="toDate">29/11</span>
    </p>
</div>
<script src="//cdnjs.cloudflare.com/ajax/libs/datejs/1.0/date.min.js" type="text/javascript"></script>
<script>
(function () {
    if (document.getElementById('fromDate')) {
        var dateStart = 6;
        var dateEnd = 12;
        var fromDate = Date.today().addDays(dateStart);
        if (fromDate.is().saturday() || fromDate.is().sunday()) {
            fromDate = fromDate.next().monday();
        }
        var toDate = Date.today().addDays(dateEnd);
        if (toDate.is().saturday() || toDate.is().sunday()) {
            toDate = toDate.next().monday();
        }
        document.getElementById('fromDate').innerHTML = fromDate.toString('dd/MM');
        document.getElementById('toDate').innerHTML = toDate.toString('dd/MM');
    }
})();
</script>
<!-- Estimated Delivery Date | b2cstory.com -->
```
