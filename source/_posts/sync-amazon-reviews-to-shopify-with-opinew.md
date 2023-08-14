---
title: 使用 Opinew 将亚马逊评论自动同步至 Shopify 独立站
date: 2022-05-03 12:50:12
tags: [Shopify,Shopify App]
categories: Shopify
cover: /sync-amazon-reviews-to-shopify-with-opinew/shopify-opinew-banner.jpg
top_img: /sync-amazon-reviews-to-shopify-with-opinew/shopify-opinew-banner.jpg
description: 本文为大家介绍了如何利用 Opinew 这款 Shopify 的评论 App 来将亚马逊产品的评论自动同步至 Shopify 独立站。
---

在上一次的文章《[使用 Elfsight 将亚马逊评论自动同步至 Shopify 独立站](https://b2cstory.com/sync-amazon-reviews-to-shopify-with-elfsight/)》中，我们介绍了如何使用 [Elfsight Amazon Reviews Widget](https://elfsight.com?ref=4894363b-e0a4-4bec-b152-292eebbba4e2) 组件来实现亚马逊与 Shopify 独立站的产品评论的自动同步，[Elfsight Amazon Reviews Widget](https://elfsight.com?ref=4894363b-e0a4-4bec-b152-292eebbba4e2) 组件的好处是价格实惠、设置方便，而且无需向我们的 Shopify 商店安装插件，仅需要在产品页面调用一段外部的代码即可迅速实现亚马逊与 Shopify 独立站的产品评论自动同步；不过 [Elfsight Amazon Reviews Widget](https://elfsight.com?ref=4894363b-e0a4-4bec-b152-292eebbba4e2) 组件的缺点也很明显，那就是仅能实现评论文字部分的同步，却无法实现评论图片的同步。这不禁令人感到很鸡肋，毕竟图文并茂的真实评论才能提高用户对我们商店以及产品的信任度，如果评论只有文字却没有图片，用户的信任度肯定会大打折扣。

在陆续测试了几款不同的评论插件后，我们终于发现了一款可以实现同时将亚马逊产品评论的图片和文字同时同步至 Shopify 商店的 App，那就是 [Opinew](https://get.shopcircle.co/ucrv0zoi7mn9)。接下来，我们详细介绍一下如何安装 [Opinew](https://get.shopcircle.co/ucrv0zoi7mn9) 并将亚马逊的产品评论导入 Shopify 商店实现亚马逊与 Shopify 的评论自动同步功能。

 ## 一、安装 Opinew

{% btn 'https://get.shopcircle.co/ucrv0zoi7mn9',点击安装 Opinew 将亚马逊评论自动同步至 Shopify ,far fa-hand-point-right,orange block center larger %}

点击上方的按钮打开 [Opinew](https://get.shopcircle.co/ucrv0zoi7mn9) 的安装界面，稍等片刻等待跳转到 Shopify 的 App Store。点击绿色的**添加应用 (Add App)** 按钮跳转到 Shopify 商店的后台进行安装，我们只需点击右上角绿色的**安装应用**按钮，然后稍等片刻等待 [Opinew](https://get.shopcircle.co/ucrv0zoi7mn9) 的安装完成即可。

![添加应用](/sync-amazon-reviews-to-shopify-with-opinew/opinew-add-app-to-shopify.jpg)

![安装应用](/sync-amazon-reviews-to-shopify-with-opinew/install-opinew-to-shopify-store.jpg)

安装完成后，会自动跳转到 [Opinew](https://get.shopcircle.co/ucrv0zoi7mn9) 的后台界面，第一次进入时，会有以下三个小步骤：

1. **Introduction：**这一步是回答三个基本的问题，随便选一下然后点击右下角的 **Continue** 按钮即可。

   ![Opinew 的小问卷](/sync-amazon-reviews-to-shopify-with-opinew/opinew-introduction.jpg)

2. **Get Set Up：**这一步是设置我们向用户发送邮件索取评论时的基本信息，分别输入商店名称、上传商店 logo、输入索评邮箱地址并设置星级的颜色即可。

   ![填写基本信息](/sync-amazon-reviews-to-shopify-with-opinew/opinew-get-set-up.jpg)

3. **Ready to Go：**这一步是选择一个订阅计划，[Opinew](https://get.shopcircle.co/ucrv0zoi7mn9) 一共有 5 个订阅计划可以选择，如果我们需要实现评论自动同步功能的话，需要选择每个月 149 美元的 Advanced 计划。

   ![选择 Advanced 订阅计划](/sync-amazon-reviews-to-shopify-with-opinew/opinew-select-a-plan.jpg)

## 二、导入亚马逊评论并设置自动同步

### 1. 导入亚马逊评论

在完成上述三个小步骤的设置后，我们会正式进入 [Opinew](https://get.shopcircle.co/ucrv0zoi7mn9) 的后台界面，我们需要点击左侧菜单栏中的 **Reviews**，然后选择 **Product Reviews**。这时，右侧区域就会显示我们 Shopify 商店中的所有商品，我们可以通过搜索框输入关键词或直接下拉找到我们需要设置的产品。

在选定产品之后我们可以看到右侧的提示内容，我们可以从亚马逊、速卖通或 eBay 进行评论导入，如果有太多的产品需要批量导入的话，我们也可以点击 **Install Now** 按钮安装一个 Chrome 浏览器的插件来更加便捷的导入评论。

![从亚马逊导入评论](/sync-amazon-reviews-to-shopify-with-opinew/opinew-import-reviews-from-amazon.jpg)

接下来，我们以导入亚马逊评论为例教大家如何进行操作。点击亚马逊的图标，在新弹窗中根据下图的中文介绍进行相关设置。然后点击右下角的 Import 按钮进行导入。

![导入亚马逊评论的相关设置](/sync-amazon-reviews-to-shopify-with-opinew/opinew-import-settings.jpg)

### 2. 开启评论自动同步

稍等片刻等评论导入成功后，我们就可以继续进行自动同步评论的设置了。

点击右上角的 **Import Settings** 按钮，在新打开的弹窗中，勾选  **Automatic Synchronization**。这样，每当我们亚马逊店铺的产品有新的评论时，[Opinew](https://get.shopcircle.co/ucrv0zoi7mn9) 就会自动帮我们同步到 Shopify 商店的对应产品评论中，避免了我们每次都需要手动导入新评论所带来的不必要的麻烦。

![点击 Import Settings 按钮](/sync-amazon-reviews-to-shopify-with-opinew/opinew-click-import-settings.jpg)

![勾选 Automatic Synchronization](/sync-amazon-reviews-to-shopify-with-opinew/opinew-select-automatic-synchronization.jpg)
