---
title: 使用 Elfsight 将亚马逊评论自动同步至 Shopify 独立站
date: 2022-04-20 18:47:51
tags: [Shopify,Shopify App]
categories: Shopify
cover: /sync-amazon-reviews-to-shopify-with-elfsight/elfsight-amazon-reviews-banner.jpg
top_img: /sync-amazon-reviews-to-shopify-with-elfsight/elfsight-amazon-reviews-banner.jpg
description: 对于很多既做亚马逊店铺又做 Shopify 独立站的卖家来说，同时管理两边的评论是一件比较麻烦的事情。特别是对于刚刚转做 Shopify 独立站的亚马逊卖家来说，新店铺没有用户积累，还无法获得有效的评论。今天就为大家介绍一款 Elfsight 的小插件，可以将我们亚马逊店铺的产品评论同步到 Shopify 店铺，既可以减少我们 Shopify 店铺产品评论维护的麻烦，又可以用已有的亚马逊产品评论作为背书，增加用户的信任度。
---

对于很多既做亚马逊店铺又做 Shopify 独立站的卖家来说，同时管理两边的评论是一件比较麻烦的事情。特别是对于刚刚转做 Shopify 独立站的亚马逊卖家来说，新店铺没有用户积累，无法迅速获得有效的评论。今天就为大家介绍一款 [Elfsight](https://elfsight.com/amazon-reviews-widget/?ref=4894363b-e0a4-4bec-b152-292eebbba4e2) 的小插件 Amazon Reviews Widget，可以将我们亚马逊店铺的产品评论自动同步到 Shopify 店铺，既可以减少我们 Shopify 店铺产品评论维护的麻烦，又可以用已有的亚马逊产品评论作为背书，增加用户的信任度。不过需要注意的是，[Elfsight](https://elfsight.com/amazon-reviews-widget/?ref=4894363b-e0a4-4bec-b152-292eebbba4e2) 的 Amazon Reviews 小插件目前只支持自动同步评论中的文本，并不支持同步评论中图片，相信随着需求的增加，[Elfsight](https://elfsight.com/amazon-reviews-widget/?ref=4894363b-e0a4-4bec-b152-292eebbba4e2) 会在以后把自动同步评论中图片的功能也会加上去。

## 一、Elfsight 账号注册

1. 点击下面按钮，打开 [Elfsight Amazon Reviews Widget](https://elfsight.com/amazon-reviews-widget/?ref=4894363b-e0a4-4bec-b152-292eebbba4e2) 的注册页面，点击右上角的 **Sign Up Free** 按钮。

{% btn 'https://elfsight.com/amazon-reviews-widget/?ref=4894363b-e0a4-4bec-b152-292eebbba4e2',注册 Elfsight 将亚马逊评论自动同步至 Shopify 独立站,far fa-hand-point-right,orange block center larger %}

![点击 Sign Up Free 按钮](/sync-amazon-reviews-to-shopify-with-elfsight/elfsight-amazon-reviews-widget-sign-up.jpg)

2. 在新页面中输入邮箱和密码，然后点击 **SIGN UP** 按钮进行注册。

![输入邮箱和密码进行注册](/sync-amazon-reviews-to-shopify-with-elfsight/elfsight-sign-up-with-email.jpg)

## 二、创建 Amazon Reviews 组件

1. 注册完成后，在 **Applications** 中选择 **Reviews** 并点击 **Amazon Reviews**，鼠标悬停后点击 **Create widget**。

![创建 Amazon Reviews 小组件](/sync-amazon-reviews-to-shopify-with-elfsight/elfsight-add-amazon-reviews-widget.jpg)

2. 在新页面的左上角，我们可以修改这个 widget 的名字，左侧则是 Elfsight 给我们提供的 12 种模版，可以让我们放在 Shopify 独立站的不同页面，如 Carousel Widget 可以放在产品页，Floating Badge 可以放在页面的左下角，Slider 可以放在主页进行展示。此处我们以 Carousel Widget 模版为例，选中之后点击左下角的 **Continue with this template** 按钮，进行详细的设置。

![Amazon Reviews 模版选择](/sync-amazon-reviews-to-shopify-with-elfsight/elfsight-select-a-template.jpg)

## 三、Amazon Reviews 组件设置

1. 先点击左侧的第一个图标 **Source**，在 Source 下方的文本框中输入我们的亚马逊产品链接，下方可以看到 [Elfsight](https://elfsight.com/amazon-reviews-widget/?ref=4894363b-e0a4-4bec-b152-292eebbba4e2) 支持的不同国家的亚马逊站点。

   另外下方还有一个 **Filters** 的选项，我们可以对评论进行以下的筛选：

   - **Show Reviews only with Text：**只显示有文字的评论
   - **Min Rating：**选择最低的评论星级
   - **Total Number of Reviews to Show：**显示评论的数量
   - **EXCLUDE REVIEWS：**排除的评论，可以根据评论者姓名或关键字进行排除
   - **INCLUDE REVIEWS：**手动添加评论，根据评论者姓名或关键字进行添加

   还可以在 **Sorting** 选项对评论进行排序，[Elfsight](https://elfsight.com/amazon-reviews-widget/?ref=4894363b-e0a4-4bec-b152-292eebbba4e2) 支持最近评论优先以及随机排序两种方式。

![评论来源设置](/sync-amazon-reviews-to-shopify-with-elfsight/elfsight-source-setting.jpg)

2. 接下来点击左侧第二个图标 **Layout** 进行布局设计，我们可以分别进行以下的设置：

   - **Layout：**布局设置，一共有 6 种选择，也可以点击 Customize 对显示的评论数量和间隔进行设置。

   - **Content Width：**自定义设置评论组件的宽度，也可以全尺寸显示

   - **Widget Title：**修改评论组件的标题及说明

   - **Header：**设置头部元素展示的内容，如标题、评分、评论数量、撰写评论按钮（会跳转到亚马逊产品页进行评论）

![评论布局设置](/sync-amazon-reviews-to-shopify-with-elfsight/elfsight-reviews-layout.jpg)

3. 完成后，点击第三个图标 **Review**，在此我们可以对评论的具体样式进行设置，如显示评论者姓名、头像、日期等等。

![评论样式设置](/sync-amazon-reviews-to-shopify-with-elfsight/elfsight-review-style-setting.jpg)

4. 然后点击第四个图标 **Appearance**，对评论组件的外观，即相关的颜色和字体进行设置。

![评论外观设置](/sync-amazon-reviews-to-shopify-with-elfsight/elfsight-review-appearance-setting.jpg)

5. 最后是第五个图标 **Settings**，我们可以设置语言、是否允许搜索引擎爬取、是否允许外链、是否允许在新窗口打开链接。

![语言等相关设置](/sync-amazon-reviews-to-shopify-with-elfsight/elfsight-settings.jpg)

6. 完成以上设置后，我们点击 **Add to website** 按钮进行添加。在添加之前，我们需要选择一个订阅计划，可以按年或按月支付，大家可以根据自己的需求进行选择。需要注意的是免费的 Lite 计划只能用于一个网站，展示次数有限制，且不能移除 [Elfsight](https://elfsight.com/amazon-reviews-widget/?ref=4894363b-e0a4-4bec-b152-292eebbba4e2) 的 logo。由于 [Elfsight](https://elfsight.com/amazon-reviews-widget/?ref=4894363b-e0a4-4bec-b152-292eebbba4e2) 除了亚马逊评论组件之外还有其他很多实用的小组件，所以如果有需要添加其他小组件的话，订阅 Apps Pack 更加划算。

![选择订阅计划](/sync-amazon-reviews-to-shopify-with-elfsight/elfsight-select-your-amazon-reviews-plan.jpg)

## 四、将 Amazon Reviews 组件添加至 Shopify 店铺

1. 选完订阅计划后，会回到我们已有的 Widgets 页面，点击 **Add to website** 按钮。

![点击 Add to website 按钮](/sync-amazon-reviews-to-shopify-with-elfsight/elfsight-my-wiggets.jpg)

2. 在弹窗中复制代码，根据以下教程按自己的需要将亚马逊评论组件添加到我们的 Shopify 店铺。

![复制代码](/sync-amazon-reviews-to-shopify-with-elfsight/elfsight-get-code.jpg)

3. 登录 Shopify 店铺后台，点击 **Online Store** 并选择 **Customize**。

![登录 Shopify 后台](/sync-amazon-reviews-to-shopify-with-elfsight/go-to-online-store-and-select-customize.png)

4. 进入页面编辑后，默认的页面是主页，我们可以点击顶部的 Home page 切换到特定的页面，然后在左侧的 Section 部分点击 **Add Section** 添加一个新的 **Custom Content** 部分。

![选择特定页面添加代码](/sync-amazon-reviews-to-shopify-with-elfsight/add-custom-content-section-to-the-target-page.jpg)

5. 移除 Custom Content 模块中的其他部分，点击 **Add content** 添加一个 **Custom HTML** 部分，然后将之前复制的代码粘贴到 HTML 的文本框中保存即可。

![点击 Add content](/sync-amazon-reviews-to-shopify-with-elfsight/add-content.png)

![添加 Custom HTML](/sync-amazon-reviews-to-shopify-with-elfsight/custom-html.jpg)

6. 这样，我们就成功地用 [Elfsight](https://elfsight.com/amazon-reviews-widget/?ref=4894363b-e0a4-4bec-b152-292eebbba4e2) 将亚马逊评论组件添加到了我们的 Shopify 独立站店铺，实现了亚马逊与 Shopify 的评论自动同步。

{% btn 'https://elfsight.com/amazon-reviews-widget/?ref=4894363b-e0a4-4bec-b152-292eebbba4e2',注册 Elfsight 将亚马逊评论自动同步至 Shopify 独立站,far fa-hand-point-right,orange block center larger %}
