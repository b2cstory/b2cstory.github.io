---
title: Shopify 独立站邮件营销教程三：使用 Omnisend 创建欢迎邮件的自动化工作流程
date: 2022-05-16 15:32:11
tags: [Shopify,Shopify App,Omnisend,邮件营销]
categories: Shopify
cover: /img/cover/omnisend-email-marketing-and-sms.jpg
top_img: /img/cover/omnisend-email-marketing-and-sms.jpg
description: 在本文中，我们将介绍如何使用 Shopify 邮件营销插件 Omnisend 的自动化邮件工作流程功能，创建一封自动发送给新订阅用户的欢迎邮件。
---

在上一篇文章《[Shopify 独立站邮件营销教程二：Omnisend 创建邮箱收集弹窗](https://b2cstory.com/email-marketing-tutorial-02-omnisend-collect-email-forms/)》中，我们介绍了如何使用 [Omnisend](https://get.omnisend.com/b2cstory) 创建一个收集用户邮箱的弹窗并应用到我们的 Shopify 独立站。当用户输入邮箱订阅后，除了能够看到订阅成功的消息以及我们设定的折扣码之外，我们也应当向用户的邮箱发送一封欢迎邮件，感谢他的订阅，同样可以附带一个折扣码，然后简单的介绍一下我们的 Shopify 商店，希望他经常光顾等等。

欢迎邮件对我们来说是极为重要的，首先一点是因为欢迎邮件的打开率相比于其他类型的邮件要更高；此外由于我们会在欢迎邮件中附带折扣码，也更容易刺激新订阅的用户进行消费；最后就是我们可以借助品牌介绍、精良的版面设计为新注册的用户留下一个良好的印象，以便于他们加深对我们品牌的认识，让他们有回购的意愿。

接下来我们就为大家介绍如何设置。

{% btn 'https://get.omnisend.com/b2cstory',立即安装注册 Omnisend 开始免费试用,far fa-hand-point-right,orange block center larger %}

## 一、创建一个欢迎邮件的自动化工作流程

首先进入 [Omnisend](https://get.omnisend.com/b2cstory) 的后台，通过顶部的导航菜单进入 Automation 模块，然后点击右侧的 **New Workflow** 按钮创建一个新的自动化邮件工作流程。

![创建新的自动化邮件工作流程](/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/omnisend-create-new-workflow.png)

在左侧的 Filter 中勾选 Welcome，可以看到 [Omnisend](https://get.omnisend.com/b2cstory) 一共为我们提供了两个默认选项，左侧的是在用户订阅后一次性发送三封欢迎邮件，右侧是只发送一封。这里我们选择只发送一封即可，一次性发送的邮件太多，用户看到了可能也会觉得反感。点击 **Customize Workflow** 按钮，进入编辑页面。

![点击 Customize Workflow 按钮](/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/omnisend-customize-workflow.png)

## 二、编辑页面介绍

可以看到该编辑页面总共分成了左、中、右三部分。

![编辑页面](/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/omnisend-workflow-editing-page.png)

其中左侧的部分是我们可以使用的各个模块，可以拖动到中间部分插入使用，我们自上而下分别进行介绍：

- **Show Stats：**查看该自动化工作流程在过去 30 天内的表现情况。
- **Email：**邮件自动化工作流程模块，即我们要自动发送给订阅用户的邮件。
- **SMS：**短信自动化工作流程模块，即我们要自动发送给订阅用户的短信。由于收集邮箱的弹窗一般不会同时收集手机号码，所以在欢迎邮件的设置中我们是不需要使用这个模块的。
- **Push Notification：**推送通知，需要有自己的手机端 App 并进行关联后才能使用。
- **Delay：**可以将邮件进行延迟发送，设置一个等待的时间。
- **Tag Contact：**可以为我们当前自动化工作流程中的用户添加一个标签，方便进行受众细分。
- **Split：**可以将流程分割成两部分，符合特定规则的用户被分成一部分，不符合规则的用户被分成另外一部分。
- **A/B Testing：**可以针对两个邮件内容样式等进行 A/B 测试。

中间的部分是我们的自动化工作流程，以从上到下的流程图的样式呈现，如果我们想在两个流程中间插入一个其他的流程，只需将左侧的对应模块拖动到对应的位置即可。

当我们在中间的部分选择了一个具体的流程后，可以在右侧的部分对该流程进行详细的设置。

## 三、自动化工作流程设置

在了解了编辑页面各个部分的内容和功能之后，接下来我们就可以针对这封欢迎邮件的自动化工作流程进行设置了。

### (1) Trigger 触发条件

第一个流程是触发条件，我们可以看到该流程的内容是当用户通过 [Omnisend](https://get.omnisend.com/b2cstory) 的邮箱收集弹窗注册后进入该流程，当用户在我们的 Shopify 独立站完成购买后则退出该流程。对于欢迎邮件，默认的设置已经足够我们使用了，一般无需进行修改。

![触发条件](/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/omnisend-trigger.png)

### (2) Delay 延迟发送

第二个流程是延迟发送，即在用户提交邮箱订阅我们的 Shopify 独立站后，我们过多久再给用户发送这封欢迎邮件。默认的延迟时间是 1 分钟，不过这个延迟是没什么必要的，因此我们可以在右侧的下拉选项框中将 Minutes 修改为 Immediately，这样我们就可以在用户提交邮箱后立即发送。需要注意的是，由于服务器等各类因素的影响，邮件的发送过程也需要一定的时间，最长可能会达到 10 分钟。不过在实际测试的过程中，一般都是会立即收到邮件的。

![延迟发送设置](/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/omnisend-delay-settings.png)

### (3) Email 邮件

第三个流程就是发送邮件了，也是自动化工作流程中最重要的一部分。

- **Subject Line：**邮件标题，我们可以点击右侧的笑脸添加表情符号，点击 `{...}` 则可以添加一些个性化的内容，比如默认标题中的 `[[account.name]]` 就是我们的账户名，后期如果我们修改了账户名，那么在欢迎邮件中，标题里的账户名也会跟着自动修改。

- **Preheader：**前言部分，紧跟在标题的后面，一般用一句简短的话即可。由于我之前在收集邮箱弹窗中写的折扣是 20%，所以在这里将默认的 10% 也修改成了 20%。

- **Sender's Name：**发件人姓名，一般写我们的品牌名称即可。

![发件人、邮件标题和前言部分](/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/omnisend-email-title-part.png)

- **Sender's Email Address：**发件人邮箱地址，一般使用域名注册的企业邮箱的地址，这边默认的邮箱地址可能是我们注册 Omnisend 时使用的邮箱地址，我们下拉选择之前设置好的企业邮箱地址即可。如果你还不知道如何设置企业邮箱地址，可以点击[这里](https://b2cstory.com/email-marketing-tutorial-01-omnisend-installation-and-introduction/#5-发件人邮箱地址)。

接着，我们点击 **Edit Content** 按钮，对欢迎邮件的内容和样式进行自定义修改。

![点击 Edit Content 按钮](/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/omnisend-edit-content.png)

可以看到邮件的编辑页面也同样是分成了三个部分，与之前一样，左侧是可以拖动使用的各种模块，可以直接选择需要的模块拖动到中间对应的位置；中间显示的是邮件的实时效果；点击中间的模块后，右侧可以对该模块进行具体的设置和内容的编辑与修改。由于 [Omnisend](https://get.omnisend.com/b2cstory) 为我们提供了几十种模块使用，我们就不一一介绍了，大家可以自己稍微摸索一下，很容易就可以上手。

![邮件编辑页面](/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/omnisend-email-editing-page.png)

这里我们简单编辑了一下邮件的样式，如下图所示：

![编辑好的邮件样式](/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/omnisend-our-email-template.png)

可以看到我们设计邮件的样式还是相对简陋，毕竟不是专业的设计人员，专业的事情还是应该交给专业的人去做。不过你也可以通过一个 Gmail 的小号去订阅竞争对手的 Shopify 独立站，通过接收他们的欢迎邮件以及其他类型的营销邮件，进行参考或是模仿。

## 四、测试欢迎邮件功能是否正常

完成邮件的编辑后，我们点击右上角的 **Finishing Editing** 按钮进行保存 。左侧还有一个 **Send Test Email** 按钮可以让我们发送测试邮件，不过接下来我们会模拟真实用户的操作进行测试，所以这里没有必要发送测试邮件。如果你确实想发一封测试邮件的话，需要注意收到的邮件中标题前面会显示 `[preview]`，另外也不会生成真实的折扣码。

![点击 Finish Editing 按钮完成设置](/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/omnisend-finish-editing.png)

回到自动化工作流程的编辑页面后，点击右上角的 **Start Workflow** 按钮，这样我们的欢迎邮件自动化工作流程就被激活了。

![点击 Start Workflow 按钮](/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/omnisend-start-workflow.png)

接下来我们按照一个正常用户的操作去进行测试。

打开 Chrome 浏览器的隐私模式，进入到我们的 Shopify 独立站，等到收集邮箱的弹窗出现后，输入我们的邮箱地址进行订阅。

![输入测试邮箱地址](/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/omnisend-input-test-email-address.png)

接着进入我们的邮箱，查看这封邮件的内容是否与我们的设置保持一致即可。这边需要检查的不只是邮件的样式，还有我们邮件中的各种链接都需要点击一遍，看看是否有跳转到对应的页面。此外，在检查完桌面端后，我们还需要在手机端打开邮件，同样的仔细检查一遍确保无误。

![检查发件人、标题和前言部分](/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/omnisend-check-sender-and-title.png)

![仔细检查邮件是否我们的设置保持一致](/email-marketing-tutorial-03-omnisend-create-a-welcome-automation/omnisend-test-email.png)

---

如果你看完本篇教程觉得 [Omnisend](https://get.omnisend.com/b2cstory) 对你 Shopify 独立站的邮件营销活动有帮助，可以点击下方的按钮选择免费的订阅计划进行试用。

{% btn 'https://get.omnisend.com/b2cstory',立即安装注册 Omnisend 开始免费试用,far fa-hand-point-right,orange block center larger %}

**相关阅读：**

1. [使用 OrderlyEmails 修改 Shopify 默认邮件模版](https://b2cstory.com/change-shopify-default-email-templates-with-orderlyemails/)

2. [Shopify 独立站邮件营销教程一：Omnisend 的安装注册与后台介绍](https://b2cstory.com/email-marketing-tutorial-01-omnisend-installation-and-introduction/)

3. [Shopify 独立站邮件营销教程二：Omnisend 创建邮箱收集弹窗](https://b2cstory.com/email-marketing-tutorial-02-omnisend-collect-email-forms/)

4. [Shopify 独立站邮件营销教程四：使用 Omnisend 设置弃购挽回邮件和弃购挽回短信的自动化工作流程](https://b2cstory.com/email-marketing-tutorial-04-omnisend-abandoned-cart-automation/)
