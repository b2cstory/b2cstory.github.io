---
title: 为 Shopify Brooklyn 主题创建新的 Collections List
date: 2021-04-07 03:10:36
updated: 2021-04-07 03:10:36
tags: [Shopify,Shopify Theme]
categories: Shopify
cover: /shopify-brooklyn-theme-new-collections-list/shopify-brooklyn-theme-cover.jpeg
top_img: /shopify-brooklyn-theme-new-collections-list/shopify-brooklyn-theme-cover.jpeg
description: 本文继续为大家介绍 Shopify Brooklyn 主题的优化 —— 创建一个新的页面展示不同的 Collections，Brooklyn 主题默认的叫法是 Collections List。
---

本文继续为大家介绍 Shopify Brooklyn 主题的优化 —— 创建一个新的页面展示不同的 Collections，Brooklyn 主题默认的叫法是 Collections List。

Brooklyn 默认的 Collections List 是只有一个的，即以 `https://xxx.com/collections` 的形式展现。而创建一个自定义的 Collections List 页面可以让你在此页面中只展示某些你选定的 Collection。例如，你可以创建一个“苹果配件”的页面，只在里边展示苹果的手机壳、AirPods 保护壳、拓展坞等相关配件的 Collection；而在另一个“三星配件”的页面，你可以选择只展示三星相关配件的 Collection。

## 一、备份主题

**在开始之前，请一定要记住先备份一下主题！**

## 二、创建 Page Template

备份完主题后，接下来我们要做的就是为自定义 Collections List 页面创建一个 Page Template。例如，我们可以创建 **page.apple-collections.liquid** 和 **page.samsung-collections.liquid** 两个模版来分别展示苹果配件和三星配件的 Collection List。进入到代码编辑区后，我们点击 **Template >> Add a New Template** 创建一个新模版，在下拉框中选择 **page** 并命名为 **apple-collection**，该名字也可以根据自己的实际需要进行更改，如下图所示。

![创建一个新的页面模版](/shopify-brooklyn-theme-new-collections-list/shopify-brooklyn-theme-create-page-template.png)

接下来，我们在搜索框中搜索 **page.full-width.liquid** 并打开，将其中的代码（或者用下方提供的代码）复制一份粘贴到我们刚刚创建的 **page.apple-collection.liquid** 模版中。

![将 page.full-width.liquid 中的代码复制到 page.apple-collection.liquid 中](/shopify-brooklyn-theme-new-collections-list/brooklyn-collection-list-copy-full-width-code.png)

```html
<!-- /templates/page.full-width.liquid | b2cstory.com -->
<header class="section-header text-center">
    <h1>{{ page.title }}</h1>
    <hr class="hr--small">
</header>

<div class="rte">
    {{ page.content }}
</div>
```

在 `{{ page.content }}` 后添新增一行，并粘贴以下调用 Section Template 的代码，如下图所示。要注意，此处的 **apple-collection-template** 要与稍后创建的新的 Section Template 名字保持一致。

```liquid
{% section 'apple-collection-template' %}
```

![添加 Section 部分的代码](/shopify-brooklyn-theme-new-collections-list/brooklyn-collection-list-add-section-code.png)

## 三、创建 Section Template

创建一个新的 Section 模版，将其命名为 **apple-collection-template**（可根据实际情况修改，但要保持与刚刚添加的调用 Section 处的名称保持一致）并将原有的代码全部删除。

![创建新的 Section 模版](/shopify-brooklyn-theme-new-collections-list/brooklyn-collection-list-create-section-template.png)

接着，我们搜索 **list-collections-template.liquid**，打开后将其中的代码复制到我们刚刚创建的 **apple-collection-template.liquid** 中。接着，我们找出下边的这部分代码将其删除。删除这部分代码是因为我们通过创建新页面调用我们刚刚的模版，标题会自动根据页面输入的标题显示，而无需使用 Collection List 自带的标题。

```html
<header class="section-header text-center">
    <h1>{{ 'collections.general.catalog_title' | t }}</h1>
    <hr class="hr--small">
</header>
```

## 四、创建新的 Collections List 页面

最后，我们就可以创建一个新的 Collections List 了。回到 Shopify 的后台，在 **Online Store >> Pages** 中创建一个新页面，将其命名为 Apple Accessories 并调用我们刚刚创建的 **apple-collection-template.liquid** 这个模版。接着，我们在 **Online Store >> Themes** 中点击 **Customize** 进行自定义设置。如下图所示，在新页面的下拉框中选择我们刚刚创建的 Apple Accessories 页面。

![选择 Apple Accessories 页面进行自定义设置](/shopify-brooklyn-theme-new-collections-list/brooklyn-customize-apple-accessories-page.png)

按照下图所示的步骤，点击 **Collections List Page**，然后选择 **Selected** 只展示选择的 Collection，接着点击 **Add Collection** 选择我们要展示的 Collection。由于我们的 Collections List 页面命名为 Apple Accessories，所以在此我们只选择 iPhone Case 和 iPad Case 这两个 Collection。设置完成后保存即可。

![选择想要展示的 Collection](/shopify-brooklyn-theme-new-collections-list/brooklyn-custom-collection-list-page-setting.png)

## 五、查看最终效果

回到 Apple Accessories 的页面编辑器，我们还可以在文本框中输入文字或是添加图片等等对该页面进行进一步的优化。保存之后可以点击 **View Page** 查看页面的效果。

![可以在内容编辑器添加文字和图片](/shopify-brooklyn-theme-new-collections-list/brooklyn-add-text-to-apple-accessories-page.png)

最终的效果如下图所示。

![最终效果](/shopify-brooklyn-theme-new-collections-list/brooklyn-apple-accessories-final-result.png)
