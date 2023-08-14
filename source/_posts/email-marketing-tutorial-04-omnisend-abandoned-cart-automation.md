---
title: Shopify 独立站邮件营销教程四：使用 Omnisend 设置弃购挽回邮件和弃购挽回短信的自动化工作流程
date: 2022-05-18 12:41:09
tags: [Shopify,Shopify App,Omnisend,邮件营销]
categories: Shopify
cover: /img/cover/omnisend-email-marketing-and-sms.jpg
top_img: /img/cover/omnisend-email-marketing-and-sms.jpg
description: 在本文中，我们将介绍如何使用 Shopify 邮件营销插件 Omnisend，为我们的独立站创建弃购挽回邮件和弃购挽回短信的自动化工作流程。
---

在上一篇文章《[Shopify 独立站邮件营销教程三：使用 Omnisend 创建欢迎邮件的自动化工作流程](https://b2cstory.com/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/)》中，我们介绍了如何使用 [Omnisend](https://get.omnisend.com/b2cstory) 为新订阅我们 Shopify 独立站的用户自动发送一封欢迎邮件，在本篇文章中则要为大家介绍另一个十分重要的邮件营销自动化工作流程 —— 弃购挽回邮件。

{% btn 'https://get.omnisend.com/b2cstory',立即安装注册 Omnisend 开始免费试用,far fa-hand-point-right,orange block center larger %}

## 一、弃购产生的原因及解决建议

弃购 (Abandoned Cart) 是指用户在我们的 Shopify 独立站中已经将商品添加到了在线购物车中，但是却没有继续结账并完成购买。根据不完全的统计，有将近 70% 的人会在结账前产生弃购，而产生弃购的原因也是多种多样的，这里我们列举一些常见的原因并给出相应的解决建议：

1. **网站加载速度太慢：**Shopify 独立站的加载速度在很大程度上会影响用户的访问体验，如果用户在访问一个页面时长时间加载不出来，可能就会直接关掉网页了。提升网站的加载速度，主要可以从以下三个角度入手。
   - **选择一个合适的主题：**不同的 Shopify 主题由于代码结构的不同，其加载速度也是不同的，所以在购买一款 Shopify 主题之前，我们需要先对该主题的 Demo 站点进行速度测试，看看是否能够达到我们的要求。常用的网站加载速度测试工具有 [PageSpeed Insights](https://pagespeed.web.dev/)、[GTmetrix](https://gtmetrix.com/)、[Pingdom Website Speed Test](https://tools.pingdom.com/) 等，大家可以从中自行选择进行测试。
   - **网站图片未经压缩：**图片的大小是影响网站加载速度最重要的因素之一，因此在我们上传图片的时候，一定要经过压缩处理，之前的文章《[Shopify 独立站图片压缩工具推荐](https://b2cstory.com/best-image-compression-tools-for-shopify/)》中有介绍几款免费的图片压缩工具，包括网页在线使用、macOS 端、Windows 端的，大家可以自行选择使用。
   - **安装的 Shopify 插件过多：**插件可以在一定程度上拓展我们 Shopify 独立站的功能，但是安装过多的插件也不可避免的会拖慢我们在线商店的速度，因此我们要尽量控制插件的安装数量，一般来说控制在 10 个以内就好，此外不需要的插件也要及时卸载并删除残留代码。

2. **运费和配送时间问题：**一般来说我们都会设置为免运费或者达到一定消费后免运费，在产品定价的时候尽量将运费包含在里边；或者提供多种配送选择，如免费但速度较慢的 E 邮宝、速度和价格都适中的 4PX 递四方或云途、价格高但速度快的 DHL 或 UPS 等，尽量让用户至少有一个免运费的选项可以选择。

3. **缺少信任徽章：**一般在产品页面购买按钮的下方，我们都会放一个信任徽章 (Trust Badge)，包括信用卡和 PayPal 的支付图标、SSL 证书、杀毒软件认证安全图标等等，以增强用户对我们 Shopify 独立站的信任感。有些付费的主题是会自带 Trust Badge 的上传选项的，如果你使用的是免费主题，也可以通过代码的形式进行添加，我们会在后期的文章中进行介绍。

   ![信任徽章 Trust Badge](/email-marketing-tutorial-04-omnisend-abandoned-cart-automation/trust-badge.png)

4. **缺少用户需要的付款方式：**一般来说，我们的在线商店只要有 [PayPal](https://www.paypal.com/) 和信用卡两种支付方式就足以满足绝大多数用户的需求了，信用卡收款一般都会选择使用 [Stripe](https://www.stripe.com/)，可以无缝集成到 Shopify 独立站中，无需跳转到第三方的页面进行付款，可以极大提升用户的购物体验。如果你有注册美国的公司，也可以添加 [Sezzle](https://sezzle.com/) 等分期付款的支付方式。

5. **缺少政策页面：**政策页面一般会放在网站底部的菜单栏，对我们独立站来说是必不可少的，如果一个用户在你的网站上没有看到政策页面，很大概率是不会在你这里消费的。常见的政策页面包括 Terms of Service、Refund Policy、Shipping Policy 等，一定要确保用户可以找得到这些页面。

## 二、使用 Omnisend 自动发送弃购挽回邮件

### (1) 关闭 Shopify 自带的弃购挽回邮件

Shopify 默认是自带发送弃购挽回邮件功能的，如果我们在 Shopify 的后台开启了**自动发送弃单营销邮件**功能的话，同时又在 [Omnisend](https://get.omnisend.com/b2cstory) 设置了弃购挽回邮件的自动化工作流程，那么用户是会同时收到 Shopify 和 [Omnisend](https://get.omnisend.com/b2cstory) 发送的弃购挽回邮件。

之所以不建议使用 Shopify 自带的弃购挽回邮件是因为 Shopify 默认的邮件模版较为简陋，如果要修改的话较为麻烦，而且 Shopify 只能发送一封弃购挽回邮件，而通过 [Omnisend](https://get.omnisend.com/b2cstory)，我们可以发送多封弃购挽回邮件，并且可以一并发送弃购挽回短信。

当然 Shopify 可以自动发送的邮件还是很多的，包括订单确认邮件、发货确认邮件等等，如果我们确实需要使用 Shopify 自带的自动发送邮件功能，可以参考《[使用 OrderlyEmails 修改 Shopify 默认邮件模版](https://b2cstory.com/change-shopify-default-email-templates-with-orderlyemails/)》对这些自带的邮件进行美化，使邮件的风格与我们的品牌保持一致。

言归正传，我们进入 Shopify 的后台，依次选择**设置 > 结账 > 弃单营销邮件**，然后取消勾选**自动发送弃单营销邮件**，如下图所示。

![弃单营销邮件设置](/email-marketing-tutorial-04-omnisend-abandoned-cart-automation/shopify-abandoned-cart-settings.png)

## 三、创建弃购挽回邮件和弃购挽回短信的自动化工作流程

进入 [Omnisend](https://get.omnisend.com/b2cstory) 的后台，通过顶部的导航菜单进入 **Automation** 模块，然后点击右侧的 **New Workflow** 按钮创建一个新的自动化工作流程。

![创建新的自动化工作流程](/email-marketing-tutorial-04-omnisend-abandoned-cart-automation/omnisend-create-new-workflow.png)

在左侧的 Filter 中勾选 **Cart Abandonment**，可以看到一共有三个默认的选项，这里我们选择中间的这个，可以发送三封弃购挽回邮件和一条弃购挽回短信。点击 **Customize Workflow** 按钮，进入编辑页面。

![点击 Customize Workflow 按钮](/email-marketing-tutorial-04-omnisend-abandoned-cart-automation/omnisend-customize-workflow.png)

进入编辑页面后，可以看到与欢迎邮件的自动化工作流程一样，同样是分为了左、中、右三个部分。

关于弃购挽回邮件的设置，由于在之前的《[Shopify 独立站邮件营销教程三：使用 Omnisend 创建欢迎邮件的自动化工作流程](https://b2cstory.com/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/)》中我们已经详细介绍过了，这里就不赘述了。不过一定要注意选中邮件模块后在右侧点击 **Edit Content** 按钮根据我们的品牌风格对邮件进行编辑，默认的邮件内容我们是无法直接使用的。

接下来主要讲一下跟设置欢迎邮件自动化工作流程不一样的地方。

### (1)  触发条件

这里我们要选择 **Abandoned Cart**，如下图所示。

![触发条件选择 Abandoned Cart](/email-marketing-tutorial-04-omnisend-abandoned-cart-automation/omnisend-edit-trigger.png)

### (2) 延迟发送

由于 Omnisend 会发送三封弃购挽回邮件和一条弃购挽回短信，所以延迟发送的时间也有四个。默认弃购挽回邮件的延迟发送时间分别为 1 小时、11 小时和 12 小时，默认弃购挽回短信的发送时间为 5 分钟，如果我们没有特殊的需要，保持默认设置即可。

### (3) 编辑弃购挽回短信

1. **Sender's Name：**即发件人姓名，这里我们输入自己的品牌名即可。

2. **Message Text：**弃购挽回短信的正文部分，这里默认是没有附带弃购挽回链接的，我们点击右侧的 `{...}` 下拉选择 **Abandoned Cart URL**，修改一下短信正文将链接添加到短信中，另外也可以加上折扣码，刺激弃购用户进行购买。下图是我们修改后的短信内容，大家可以拿来参考。

   ![修改短信内容](/email-marketing-tutorial-04-omnisend-abandoned-cart-automation/omnisend-message-text.png)

3. **Add Image/GIF：**在短信正文附带图片或 GIF，只有美国或者加拿大的号码才可以收到。

4. 剩下的三个选项默认勾选即可，分别是自动使用短链接，避免短信内容过长；为美国和加拿大的收信人开启退订选项；为非美国和加拿大的用户开启退订选项。

5. 在 **PREVIEW AS** 部分我们可以预览当前的短信，其中底部的 Characters 是我们当前短信的字符数，一条短信最多可以有 160 个字符，如果超过了则会被拆分成两条短信发送。

   ![预览当前短信](/email-marketing-tutorial-04-omnisend-abandoned-cart-automation/omnisend-message-preview.png)

设置完成后我们点击右下角的 **Update** 按钮进行保存。然后点击右上角的 **Start Workflow** 按钮即可开始运行该自动化工作流程。

![开启自动化工作流程](/email-marketing-tutorial-04-omnisend-abandoned-cart-automation/omnisend-start-workflow.png)

## 四、测试弃购邮件和弃购短信功能是否正常

完成相关的设置之后，我们在 Chrome 浏览器的隐私窗口打开自己的 Shopify 独立站，模拟一个正常用户的下单流程进行测试弃购功能。

选中一个产品后，点击 **Buy It Now** 按钮，然后在新页面输入我们的联系方式。其中我们需要勾选 **Email me with news and offers** 以及下方的 **Text me with news and offers**，并确保输入准确的邮箱地址和手机号码，这样之后我们在做邮件营销和短信营销的活动时，可以通过该邮箱和电话来接收对应的营销信息，来检查我们的营销内容是否无误。

![填写结账信息](/email-marketing-tutorial-04-omnisend-abandoned-cart-automation/shopify-checkout-information.png)

点击 **Continue to Shipping** 按钮进入下一步，然后再点击 **Continue to Payment** 按钮。进入到支付页面之后，我们就可以关闭了，或者输入错误的信用卡信息进行提交。因为到这一步已经足够我们测试弃购邮件和短信的功能了。

![点击 Continue to Payment 按钮](/email-marketing-tutorial-04-omnisend-abandoned-cart-automation/shopify-shipping-information.png)

由于之前我们设置的邮件发送时间分别为 1 小时、11 小时和 12 小时，我们可以等第二天的时候再查看邮件和短信，看看能否正常接收到。

这里我们为了测试功能，设置的邮件发送时间分别为 1 分钟、2 分钟和 3 分钟，可以看到已经收到了三封邮件，由于服务器延迟等各类因素的影响，邮件发送过程本身也需要一定的时间，不过这个时间误差还是在可以接受的范围之内的。

![收到的三封弃购挽回邮件](/email-marketing-tutorial-04-omnisend-abandoned-cart-automation/abandoned-cart-emails-sent-by-omnisend.png)

此外，我们也可以在 [Omnisend](https://get.omnisend.com/b2cstory) 的后台点击顶部菜单的 **Reports**，在左侧菜单选择 **Workflows**，然后在 Abandoned Cart 右侧点击 **View Report** 按钮查看报告。

![查看 Workflows 报告](/email-marketing-tutorial-04-omnisend-abandoned-cart-automation/omnisend-reports-of-workflows.png)

在 **Workflow Overview** 模块的下方，我们可以看到该弃购挽回自动化工作流程的运行状态。

![查看弃购挽回自动化工作流程的运行状态](/email-marketing-tutorial-04-omnisend-abandoned-cart-automation/omnisend-workflow-overview.png)

---

如果你看完本篇教程觉得 [Omnisend](https://get.omnisend.com/b2cstory) 对你 Shopify 独立站的邮件营销活动有帮助，可以点击下方的按钮选择免费的订阅计划进行试用。

{% btn 'https://get.omnisend.com/b2cstory',立即安装注册 Omnisend 开始免费试用,far fa-hand-point-right,orange block center larger %}

**相关阅读：**

1. [使用 OrderlyEmails 修改 Shopify 默认邮件模版](https://b2cstory.com/change-shopify-default-email-templates-with-orderlyemails/)

2. [Shopify 独立站邮件营销教程一：Omnisend 的安装注册与后台介绍](https://b2cstory.com/email-marketing-tutorial-01-omnisend-installation-and-introduction/)

3. [Shopify 独立站邮件营销教程二：Omnisend 创建邮箱收集弹窗](https://b2cstory.com/email-marketing-tutorial-02-omnisend-collect-email-forms/)

4. [Shopify 独立站邮件营销教程三：使用 Omnisend 创建欢迎邮件的自动化工作流程](http://localhost:4000/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/)

