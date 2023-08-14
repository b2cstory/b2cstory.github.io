---
title: 用 Shopify 的 Form Builder App 为 Etsy 的定制产品创建图片上传页面
date: 2021-04-03 02:39:18
updated: 2021-04-03 02:39:18
tags: [Shopify,Shopify App]
categories: Shopify
cover: /shopify-app-form-builder/shopify-app-form-builder-cover.png
top_img: /shopify-app-form-builder/shopify-app-form-builder-cover.png
description: 本文为大家介绍的是如何解决 Etsy 的顾客在购买定制产品的时候上传图片的问题。本文中提到的方法主要是针对既在 Etsy 开店又有自己 Shopify 独立站的卖家，需要用到一款由 HulkApps 开发的叫做 Form Builder with File Upload 的 App。
---

本文为大家介绍的是如何解决 Etsy 的顾客在购买定制产品的时候上传图片的问题。本文中提到的方法主要是针对既在 Etsy 开店又有自己 Shopify 独立站的卖家，需要用到一款由 [HulkApps](https://www.hulkapps.com/?ref=shadow&utm_source=chrischow1&utm_campaign=HulkApps+Partner+Program) 开发的叫做 [Form Builder with File Upload](https://formbuilder.hulkapps.com/login/?ref=shadow) 的 App。

对于在 Etsy 出售图片定制类产品的卖家来说，目前主流的方法是让顾客通过 Etsy Messenger 发送想要定制的图片，更进一步者，会选择在产品介绍里留下自己的邮箱并让顾客选择通过邮件发送图片，这两种方法都不失为有效可行的方法。然而，根据来自 Tamebay 网站中一篇关于三个平台定制产品的对比《[Custom made items: eBay, Amazon and Etsy compared](https://tamebay.com/2017/05/custom-made-items-ebay-amazon-and-etsy-compared.html)》显示，虽然通过  Etsy Messenger 发送的图片尺寸没有被调整过，但是却被压缩了。

> The results from Etsy are interesting, the image is compressed but it’s not resized. The image size was retained at 5312 × 2988 pixels. The DPI remained at 72 but the file size reduced from 4.32 MB to 2.55 MB. This is a lossy compression, where some information in the file has been deleted and so the picture isn’t quite as sharp as the original. However due to the original file size I couldn’t detect any difference on a computer screen – it may make a difference if you’re ordering a five foot poster print, but for most purposes it’s safe to say that images sent through Etsy are perfectly usable.

测试图片的尺寸仍然保留在 5312 × 2988 像素，DPI 也保持在 72，但是文件的大小却从原来的 4.32 MB 减少到了 2.55 MB。这是很明显的有损压缩，图片中的某些细节在压缩过程中被移除了，因此收到的图片看起来也不如原来那么清晰。虽然对于定制小尺寸产品来说这点细节的损失可能影响不是很大，但如果顾客是定制的比较大的尺寸，比如打印一张五英寸的海报，损失的细节看起来就会比较明显了。

通过邮件发送的话多了一步顾客在新窗口打开邮箱并发送的操作，而你能收到的也只是顾客发送的一张图片而已。既然如此，我们为何不更进一步，在自己的 Shopify 独立站上单独打造一个页面，让在 Etsy 下单了定制产品的顾客来到我们的 Shopify 独立站上传图片呢？如此一来，不仅可以解决图片被压缩的问题，还可以将 Etsy 的顾客转化为我们 Shopify 独立站的潜在用户。要知道在 Shopify 独立站上刺激消费者下单的方式远比 Etsy 要多，可以通过各种 Upsell 提高客单价，也可以把顾客加入 Shopify 独立站的 EDM 系统定期推送新产品等等，可谓是一举多得。

接下来，还是以 [Turbo Portland 主题](https://outofthesandbox.com/products/turbo-theme-portland?rfsn=4714227.94d985b&utm_source=refersion&utm_medium=affiliate&utm_campaign=4714227.94d985b)为例，为大家详细的介绍如何通过 [Form Builder with File Upload](https://formbuilder.hulkapps.com/login/?ref=shadow) 创建单独的页面，让 Etsy 的顾客可以在我们的 Shopify 独立站上提交定制图片。

## 一、安装 Form Builder with File Upload

点击下方的按钮，进入下图所示界面，输入我们的店铺地址再点击 Install 按钮跳转到 Shopify 后台的应用安装界面。

{% btn 'https://formbuilder.hulkapps.com/login/?ref=shadow',立即安装 Form Builder with File Upload｜为 Shopify 店铺创建图片上传页面,far fa-hand-point-right,orange block center larger %}

![输入店铺地址进行安装](/shopify-app-form-builder/shopify-form-builder-enter-your-shopify-domain.png)

再点击 Install App，完成 [Form Builder with File Upload](https://formbuilder.hulkapps.com/login/?ref=shadow) 在自己 Shopify 店铺的安装。

![点击 Install App 将 Form Builder with File Upload 安装到 Shopify 店铺](/shopify-app-form-builder/shopify-install-form-builder-with-file-upload-app.png)

## 二、创建图片上传表单

安装完成后，会自动跳转到 [Form Builder with File Upload](https://formbuilder.hulkapps.com/login/?ref=shadow) 的后台界面。我们点击 Create New Form 或是 New Form 按钮开始创建新的表单。

![点击 Create New Form 创建新的表单](/shopify-app-form-builder/hulkapps-form-builder-dashboard.png)

在新页面中，点击 Blank Form 创建一个空白的表单。

![点击 Blank Form 创建一个空白表单](/shopify-app-form-builder/hulkapps-create-blank-form.png)

接下来，我们可以看到创建一个新的表单只需要 CONNECT >> CONTENT >> DESIGN 这三步。

![只需三步设置即可创建完表单](/shopify-app-form-builder/shopify-hulkapps-form-builder-steps.png)

### 1. CONNECT

- **Form Details:** 需要填写表单名称（Form Name）和接收通知的邮件地址（Notification Email Addresses）；
- **Form Schedule:** 设置表单的起止日期，这个我们用不到可以直接跳过；
- **Shopify Integration:** 可以为提交表单的 Etsy 顾客自动创建我们 Shopify 店铺的账户以及发送激活账户的邮件，如果想要把 Etsy 的顾客转化为我们 Shopify 店铺的用户，可以勾选这两项；
- **Mail Integration:** 可以接入 [Mailchimp](https://mailchimp.com/) 或是 [Klaviyo](https://www.klaviyo.com/partner/signup?utm_source=0013o00002Vl2pc&utm_medium=partner) 这两个邮件营销的应用；
- **Payment Integration:** 可以接入 Stripe。

### 2. CONTENT

- **Form Settings:** 表单的标题（Form Title），描述（Description）以及提交按钮的文本（Submit Button Text）；
- **Form Element:** 需要顾客填写的内容，可以根据自己的需求进行组合；
- **Captcha:** 谷歌 “I’m not a robot” 验证；
- **Customize Form Messages:** 自定义表单消息，一般情况下无需修改；
- **Customize Form Scrolling:** 自定义表单滚动，即表单提交报错或者提交成功后自动返回顶端；
- **After Submit:** 设置表单提交成功后显示的内容；
- **Auto Responder:** 设置自动回复；
- **Admin Email:** 配置表单元素回复顾客邮件。

### 3. DESIGN

- **Layout:** 设置表单布局；
- **Form:** 设计样式，背景、阴影、宽度等等；
- **Input:** 设置输入部分的样式；
- **Submit Button:** 设置提交按钮的样式；
- **Advanced:** 高级设置，关联 Google Analytics Tracking ID 和 Facebook Pixel ID 等。

在本案例中，我们主要添加了以下 Form Element，其他部分并未进行改动。

![本案例中添加的 Form Element](/shopify-app-form-builder/shopify-form-builder-form-element.png)

## 三、创建表单页面

当我们将表单设计完成后，可以点击底部的 Publish 进行发布。接着会跳转到 Current Forms 页面，这个页面会显示我们目前已经创建过的表单。我们点击复制的按钮，复制 Form Builder 生成的短代码。

![点击复制按钮复制表单代码](/shopify-app-form-builder/shopify-form-builder-current-forms.png)

接下来，我们在 Shopify 店铺的后台创建一个新页面（Online Store >> Pages >> Add Page），点击右侧的代码图标进入代码编辑模式后，将刚才复制的短代码粘贴到编辑器中并保存。这样，一个可以让用户上传图片的表单页面就制作完成了。

![进入页面的代码编辑模式，将刚才复制的代码粘贴至其中](/shopify-app-form-builder/shopify-add-upload-picture-page.png)

完成后的页面如下图所示。

![表单的最终效果](/shopify-app-form-builder/shopify-upload-picture-page.png)

## 四、提交测试表单

最后，我们需要填入信息测试一下表单功能是否正常。填入信息提交后，我们回到 Form Builder with File Upload 的后台，点击 Customize Form。

![点击 Customize Form 查看测试表单](/shopify-app-form-builder/shopify-form-builder-customize-form.png)

可以看到 No. of Responses 显示的数量为 1，说明我们刚刚的表单提交成功了。然后再点击 Submitted Responses 检查一下信息是否正确，图片能否正常下载即可。

![检查一下表单信息是否正确](/shopify-app-form-builder/hulkapps-form-builder-submitted-responses.png)

如果你觉得这款由 HulkApps 出品的 [Form Builder with File Upload](https://formbuilder.hulkapps.com/login/?ref=shadow) 对你有所帮助，不妨点击下面的按钮立刻体验吧！

{% btn 'https://formbuilder.hulkapps.com/login/?ref=shadow',立即安装 Form Builder with File Upload｜为 Shopify 店铺创建图片上传页面,far fa-hand-point-right,orange block center larger %}
