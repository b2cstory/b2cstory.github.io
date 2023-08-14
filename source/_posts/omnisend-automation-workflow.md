---
title: Omnisend 如何设置邮件自动化工作流 —— 以弃购挽回邮件为例
date: 2021-06-02 03:32:11
updated: 2021-06-02 03:32:11
tags: [Shopify,Shopify App,Omnisend,邮件营销]
categories: Shopify
cover: /omnisend-automation-workflow/omnisend_automation_library.jpeg
top_img: /omnisend-automation-workflow/omnisend_automation_library.jpeg
description: 本文以订单确认邮件为例，为大家介绍如何设置 Omnisend 的邮件自动化工作流。
---

{% note warning flat %}
使用 Omnisend 进行 Shopify 独立站邮件营销的教程已经更新，你可以参考最新的教程进行设置：

1. [Shopify 独立站邮件营销教程一：Omnisend 的安装注册与后台介绍](https://b2cstory.com/email-marketing-tutorial-01-omnisend-installation-and-introduction/)
2. [Shopify 独立站邮件营销教程二：Omnisend 创建邮箱收集弹窗](https://b2cstory.com/email-marketing-tutorial-02-omnisend-collect-email-forms/)
3. [Shopify 独立站邮件营销教程三：使用 Omnisend 创建欢迎邮件的自动化工作流程](https://b2cstory.com/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/)
4. [Shopify 独立站邮件营销教程四：使用 Omnisend 设置弃购挽回邮件和弃购挽回短信的自动化工作流程](https://b2cstory.com/email-marketing-tutorial-04-omnisend-abandoned-cart-automation)
5. [使用 OrderlyEmails 修改 Shopify 默认邮件模版](https://b2cstory.com/change-shopify-default-email-templates-with-orderlyemails/)

{% endnote %}

在今天的文章中，我们将以弃购挽回邮件为例，继续为大家介绍如何设置 [Omnisend](https://get.omnisend.com/b2cstory) 的邮件自动化工作流。如果你是刚刚开始接触邮件营销，可以点击下面的按钮将 [Omnisend](https://get.omnisend.com/b2cstory) 安装到你的 Shopify 独立站上，具体的安装教程以及对 [Omnisend](https://get.omnisend.com/b2cstory) 的介绍可以参考上一篇博文《[Shopify 邮件营销插件 Omnisend Email Marketing 使用教程](https://b2cstory.com/shopify-app-omnisend-email-marketing-tutorial/)》。

{% btn 'https://get.omnisend.com/b2cstory',立即注册 Omnisend 开启 14 天免费试用,far fa-hand-point-right,orange block center larger %}

在正式开始之前，先说一些题外话。之前曾经关注过很多国内、国外的独立站，通过模拟真实顾客的下单流程订阅了他们的网站，几天之后，我的测试邮箱就被这些独立站的弃购和推广邮件塞满了。如果你对邮件营销并不是很了解，可以通过这种方法订阅竞争对手的独立站来获取他们的邮件信息作为参考。

不过，我想强调的重点是在我点开这些邮件查看内容时，发现国内很大一部分独立站的卖家都是使用的 Shopify 自带的邮件模版，即便有安装 [Omnisend](https://get.omnisend.com/b2cstory) 这类的邮件营销插件，也基本上是用来手动发送节日活动之类的推广邮件，对于系统自动发送的弃购挽回、发货确认等邮件，仍然在用 Shopify 自带的邮件模版。

如果你是站群卖家或是爆款卖家，你的主要精力可能不会放在这里。但是对于想做垂直精品独立站的卖家来说，这些自动发送的邮件模版是值得你花精力去优化的，精品站的一大优势就是差异化，而差异化并不应该仅限于产品本身，更应该让顾客在你网站下单的整个流程中都感受到你的独立站的与众不同，这样顾客才愿意记住你的品牌并来你这里消费。

接下来进入本文正式内容。

## 一、注意事项

首先，有以下几点是需要注意的：

1. 只有免费试用版与付费订阅版（Standard, Pro, Enterprise）的用户才可以使用 Omnisend 的弃购挽回邮件自动化工作流；
2. 如果你的 Omnisend 有添加员工账户的话，要注意只有权限为 Analyst 之外的用户才可以编辑邮件自动化工作流；
3. 默认设置是只有订阅用户和非订阅用户才能收到弃购挽回邮件，如果是在收到邮件后手动点了 Unsubscribe，那么他是无法收到弃购挽回邮件的。

## 二、验证发件人邮箱地址

在开始设置弃购挽回邮件模版前，我们需要先验证一下发件人的邮箱地址，即用哪个邮箱地址去发送这些邮件。在 Omnisend 后台点击右上角头像的部分，然后打开 Store Settings >> Settings >> Channel Settings，如下图所示。

![打开 Channel Settings](/omnisend-automation-workflow/omnisend-channel-settings.png)

在 Channel Settings 中，点击右下角绿色的 ADD SENDER'S EMAIL ADDRESS 按钮，并在新页面中输入邮箱地址点击 Save 保存。这里需要注意的是输入的邮箱地址最好以自己的域名为后缀，如 `support@b2cstory.com`，如果使用 `b2cstory@gmail` 或是 `b2cstory@hotmail.com` 等后缀的邮箱地址，可能会无法绑定，亦或者绑定成功但发出去的邮件会被自动退回。

![点击 ADD SENDER'S EMAIL ADDRESS 按钮](/omnisend-automation-workflow/omnisend-add-sender-s-email-address.png)

接下来点击右下角的 Verify Email。

![点击 Verify Email](/omnisend-automation-workflow/omnisend-verify-email.png)

再点击 SEND VERIFICATION EMAIL 发送验证邮件。

![点击 SEND VERIFICATION EMAIL 发送验证邮件](/omnisend-automation-workflow/omnisend-send-verification-email.png)

在收件箱中打开验证邮件进行验证即可，如果收件箱里没有，可以去垃圾邮件里找一下。

## 三、设置弃购挽回邮件模版

回到 Omnisend 的后台，点击 Automation 再点击右侧的 + New Workflow 按钮。

![点击 + New Workflow 创建新的自动化工作流](/omnisend-automation-workflow/omnisend-automation-create-new-workflow.png)

接着在 Type 中勾选 Cart Abandonment，然后在右侧选择自动发送三封邮件的这个 Workflow。

![选择自动发送三封邮件的 Abandoned Cart Workflow](/omnisend-automation-workflow/create-abandon-cart-workflow.png)

如下图所示，进入到编辑页面后，可以看到默认会发送三封弃购挽回邮件，分别是 1 小时后、11 小时后、12 小时后。前两封邮件的内容是提醒顾客有东西落在购物车了，让他们付款完成购买，第三封则会由 Omnisend 生成一个折扣码，为挽回弃购做最后的尝试。

![弃购挽回邮件工作流程图](/omnisend-automation-workflow/omnisend-abandoned-cart-workflow.png)

当然，我们也可以根据自己的实际需求自定义邮件发送的时间以及邮件的内容。如下图所示，如果要修改邮件发送时间，我们只需要点击流程图中的时间模块，并在右侧的设置界面选择我们想要发送的时间即可。

![修改邮件到发送时间](/omnisend-automation-workflow/omnisend-sending-time.png)

对于邮件模版的内容，我们也可以在很大的程度上进行自定义设置。我们以第三封邮件模版为例，选中流程图中第三封邮件的模块，在右侧的编辑界面中，可以分别设置**邮件标题**、**邮件预览内容**、**发送者名称**、**发送者邮箱地址**等。

![编辑邮件相关信息](/omnisend-automation-workflow/omnisend-edit-email.png)

如果要对邮件的内容进行编辑，我则需要点击 Edit Content 这个按钮。在新页面中，我们可以看到左侧为邮件内容的预览，右侧为设置界面。先看右侧的设置界面，分为 **CONTENT** 和 **DESIGN** 两部分，在 CONTENT 中，我们可以在 Standard Blocks 中选择需要的模块拖动到左侧的内容预览区域，Omnisend 默认有 19 种模块供我们选择，对于绝大部分卖家来说都是足够用的了。而 Saved Blocks 则是我们自己保存的模块，例如我们在左侧对现有的模块进行编辑后，想将该编辑好的模版用到以后的邮件中，就可以先保存该模块，下次直接在 Saved Blocks 中调用。

![编辑邮件模版](/omnisend-automation-workflow/omnisend-edit-content.png)

对于左侧的内容部分，我们只需点击需要修改的模块并在右侧的 CONTENT 中修改相应的内容即可，此外，还有 SETTINGS 和 CONDITIONS，可以分别设置样式及一些限定条件等等，如下图所示。图片中红色方块标注的部分是保存的按钮，即上文中提到的可以将编辑好的模块保存到 Saved Blocks 中方便以后调用。

![对具体模块进行编辑](/omnisend-automation-workflow/omnisend-edit-email-template.png)

对于具体的颜色，边距等很细节的部分，本文就不具体展开了，毕竟不同的人有不同的需求，还是要根据自己的偏好及网站的风格去自己摸索。

设置完成后，我们可以点击右下角的 SAVE & GO BACK 按钮进行保存。不过在此之前，建议点击左侧的预览或是发送测试邮件先把邮件内容检查一遍，确认无误后再进行保存。

![img](/omnisend-automation-workflow/omnisend-finish-editing-email-template.png)

关于 Omnisend 设置邮件自动化的工作流就介绍到这里，如果你觉得 Omnisend 可以满足你进行邮件营销的需求，可以点击下面的按钮注册并体验，基本的安装使用教程可以参考上一篇文章《 [Shopify 邮件营销插件 Omnisend Email Marketing 使用教程](https://b2cstory.com/shopify-app-omnisend-email-marketing-tutorial/) 》。

{% btn 'https://get.omnisend.com/b2cstory',立即注册 Omnisend 开启 14 天免费试用,far fa-hand-point-right,orange block center larger %}
