---
title: Shopify 独立站邮件营销教程二：Omnisend 创建邮箱收集弹窗
date: 2022-05-13 21:32:11
tags: [Shopify,Shopify App,Omnisend,邮件营销]
categories: Shopify
cover: /img/cover/omnisend-email-marketing-and-sms.jpg
top_img: /img/cover/omnisend-email-marketing-and-sms.jpg
description: 在本文中，我们将介绍如何使用邮件营销插件 Omnisend 为 Shopify 独立站创建邮箱收集弹窗，以便于我们日后进行邮件营销活动。
---

在上一篇文章《[Shopify 独立站邮件营销教程一：Omnisend 的安装注册与后台介绍](https://b2cstory.com/email-marketing-tutorial-01-omnisend-installation-and-introduction/)》中，我们详细介绍了 [Omnisend](https://get.omnisend.com/b2cstory) 的安装注册方法、完成安装后的基本设置以及后台各个部分的功能。这一篇文章主要为大家介绍如何在 [Omnisend](https://get.omnisend.com/b2cstory) 设置弹窗注册表单并将其添加到我们 Shopify 独立站。

{% btn 'https://get.omnisend.com/b2cstory',立即安装注册 Omnisend 开始免费试用,far fa-hand-point-right,orange block center larger %}

## 一、两种常见的邮箱收集弹窗

目前 Shopify 独立站常见的邮箱收集弹窗有两种样式，一种是比较常见的，弹出来一个小框框，告诉我们用邮箱注册后可以获得一个折扣码或其他优惠，如下图所示。

![常见的弹窗样式](/email-marketing-tutorial-02-omnisend-collect-email-forms/shopify-common-pop-up.png)

另一种样式则是像大转盘抽奖一样，在访问页面时弹出来一个幸运转盘，输入邮箱后可以抽奖，奖项包括 Free Shipping、10% OFF、20% OFF 等等。

![大转盘型的弹窗样式](/email-marketing-tutorial-02-omnisend-collect-email-forms/shopify-wheel-pop-up.png)

有时候我们使用的 Shopify 主题是自带了邮箱收集弹窗功能的，另外也有一些第三方的 Shopify 插件可以制作不同类型的弹窗。不过为了避免安装过多插件拖慢网站速度，也为了更好的利用 [Omnisend](https://get.omnisend.com/b2cstory) 做好邮件营销活动，我们还是推荐使用 [Omnisend](https://get.omnisend.com/b2cstory) 的弹窗功能来收集用户的邮箱。

## 二、Omnisend 邮箱收集弹窗设置教程

在 [Omnisend](https://get.omnisend.com/b2cstory) 后台点击顶部菜单的 Forms，我们可以直接点击绿色的 **Preview and Launch Form** 按钮快速创建邮箱收集弹窗，也可以点击底部的 **View Other Form Types** 链接查看所有的模版，然后从中挑选一个自己喜欢的，其中大转盘抽奖形式的模版要下拉到最下方才能看到。

![创建邮箱收集弹窗](/email-marketing-tutorial-02-omnisend-collect-email-forms/omnisend-forms.png)

这里我们点击 **Preview and Launch Form** 按钮进行创建即可。

### (1) Theme

进入到编辑页面后，可以看到左侧是邮箱收集弹窗的样式，其中上方的 Form 和 Success 分别表示输入邮箱订阅前后的样式，我们可以点击分别查看；右侧则可以进行一些自定义的设置，如下图所示。

![邮箱收集弹窗编辑页面](/email-marketing-tutorial-02-omnisend-collect-email-forms/omnisend-form-design-page.png)

这里我们将 Topic 选择 **Discount Offer**，Layout 选择 **Background Image** 然后在弹窗中点击 **REPLACE IT** 按钮替换当前设置，Theme 的话就选择第一个。设置完成后邮箱收集弹窗变成了如下的样式。

![修改后的邮箱收集弹窗样式](/email-marketing-tutorial-02-omnisend-collect-email-forms/monisend-custom-form-style.png)

### (2) Content & Design

接着我们点击右下角的 **EDIT CONTENT** 按钮，可以看到右侧的编辑界面分成了 Content 和 Design 两个选项。

首先是 Content 部分，这个可以自定义的内容很多，我们就挑几个比较重要的跟大家说一下，具体见下图。这里我们将折扣比例改为了 20%，一般为了吸引新用户注册，折扣力度可以大一点，另外我们在订阅成功的消息内添加了折扣码，这个折扣码需要我们自己在 Shopify 独立站的后台进行设置。

![自定义内容](/email-marketing-tutorial-02-omnisend-collect-email-forms/omnisend-content-settings.png)

接着是 Design 部分，我们可以调整弹窗在页面的位置，修改字体和颜色，取消 Omnisend Logo 的勾选 (该功能需付费订阅) 来移除弹窗底部的 Powered by Omnisend。

![自定义设计](/email-marketing-tutorial-02-omnisend-collect-email-forms/omnisend-design-settings.png)

修改完成后，我们点击右下角的 **SAVE & PROCEED** 按钮保存并进行下一步。

### (3) Settings

1. **Tag：**我们可以将通过弹窗注册的用户添加一个标签，方便后期进行受众细分。

   ![标签](/email-marketing-tutorial-02-omnisend-collect-email-forms/omnisend-form-settings-tag.png)

2. **Double Opt-in：**用户通过弹窗注册后，需要去邮箱确认才能进入我们的订阅列表。由于这会增加用户订阅的难度，因此无需勾选。

   ![双重确认](/email-marketing-tutorial-02-omnisend-collect-email-forms/omnisend-form-settings-double-opt-in.png)

3. **Timing：**可以设置弹窗在什么时间显示。默认是用户访问网站后立即显示，我们也可以设置成以下显示方式：

   - 用户访问了几个页面后再显示弹窗
   - 用户在一个页面上看了几秒后再显示弹窗
   - 用户在一个页面下拉了一定的比例后再显示弹窗
   - 用户将要离开我们的商店时显示弹窗

   ![弹窗显示时间](/email-marketing-tutorial-02-omnisend-collect-email-forms/omnisend-form-settings-timing.png)

   ![弹窗显示时间详细设置](/email-marketing-tutorial-02-omnisend-collect-email-forms/omnisend-form-settings-timing-details.png)

4. **Targeting：**可以针对特定的页面显示或不显示弹窗。

   ![特定页面显示弹窗](/email-marketing-tutorial-02-omnisend-collect-email-forms/omnisend-form-settings-targeting.png)

   ![特定页面显示弹窗详细设置](/email-marketing-tutorial-02-omnisend-collect-email-forms/omnisend-form-settings-targeting-details.png)

5. **Limits：**对没有订阅的用户，设置几天后再重新显示弹窗。

   ![时间限制](/email-marketing-tutorial-02-omnisend-collect-email-forms/omnisend-form-settings-limits.png)

设置完成后，我们点击右下角的 **SAVE & PROCEED** 按钮保存并进行下一步。

### (4) Confirm & Launch

这里我们可以查看之前的设置，如果确认没有问题的话，我们可以直接点击右下角的 **SAVE & ENABLE** 按钮进行发布。

![确认并发布](/email-marketing-tutorial-02-omnisend-collect-email-forms/omnisend-confirm-and-launch.png)

## 三、检查弹窗是否正常显示

最后，我们打开浏览器进入隐私模式，访问我们的 Shopify 独立站，看看邮箱收集弹窗是否可以正确显示。然后再输入一个邮箱小号注册，检查是否一切正常即可。

![检查弹窗是否正常显示](/email-marketing-tutorial-02-omnisend-collect-email-forms/visit-our-shopify-store.png)

---

如果你看完本篇教程觉得 Omnisend 对你 Shopify 独立站的邮件营销活动有帮助，可以点击下方的按钮选择免费的订阅计划进行试用。

{% btn 'https://get.omnisend.com/b2cstory',立即安装注册 Omnisend 开始免费试用,far fa-hand-point-right,orange block center larger %}

**相关文章：**

1. [使用 OrderlyEmails 修改 Shopify 默认邮件模版](https://b2cstory.com/change-shopify-default-email-templates-with-orderlyemails/)
2. [Shopify 独立站邮件营销教程一：Omnisend 的安装注册与后台介绍](https://b2cstory.com/email-marketing-tutorial-01-omnisend-installation-and-introduction/)
3. [Shopify 独立站邮件营销教程三：使用 Omnisend 创建欢迎邮件的自动化工作流程](https://b2cstory.com/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/)
4. [Shopify 独立站邮件营销教程四：使用 Omnisend 设置弃购挽回邮件和弃购挽回短信的自动化工作流程](https://b2cstory.com/email-marketing-tutorial-04-omnisend-abandoned-cart-automation/)