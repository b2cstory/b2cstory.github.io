---
title: 如何为 Shopify 独立站的产品页添加 Buy on Amazon 按钮
date: 2022-05-11 11:49:36
tags: [Shopify]
categories: Shopify
cover: /create-a-buy-on-amazon-button-for-shopify-store/create-buy-on-amazon-button-banner.png
top_img: /create-a-buy-on-amazon-button-for-shopify-store/create-buy-on-amazon-button-banner.png
description: 本文为大家介绍如何通过代码无需安装插件 (App) 为 Shopify 独立站的产品详情页创建一个 Buy on Amazon 的按钮，通过在 Shopify 独立站产品编辑页面的 SKU 或 Barcode 处输入亚马逊对应的产品链接，我们可以实现点击 Buy on Amazon 按钮后跳转到对应的亚马逊产品，使 Shopify 独立站的产品和亚马逊店铺的产品保持一一对应。
---

很多跨境电商的卖家可能既是亚马逊的卖家，也是 Shopify 独立站的卖家。有些卖家的 Shopify 独立站可能在运营的同时也希望为自己的亚马逊店铺引流，让用户既可以在 Shopify 独立站下单，也可以去到自己的亚马逊店铺下单。这样一来，在 Shopify 独立站的产品页添加一个 **Buy on Amazon** 的按钮就必不可少了。本文为大家介绍几种方法来在产品页添加 **Buy on Amazon** 按钮，即便有很多个产品，也可以实现将 Shopify 独立站的产品与亚马逊店铺的产品一一对应，方便用户在自己喜欢的平台进行下单。

## 一、找到合适的按钮图案并上传至 Shopify 后台

首先，我们打开谷歌图片搜索，在搜索框中输入 "buy on amazon button"，然后找一个自己喜欢的按钮图片下载，图片格式的话尽量选择 PNG 或是 JPG。

![谷歌图片搜索 buy on amazon button](/create-a-buy-on-amazon-button-for-shopify-store/google-images-search-buy-on-amazon-button.png)

比如我们找到了下面这张 PNG 格式的图片将其下载下来，并将其重命名为 "buy-now-on-amazon-button.png"。

![Buy Now on Amazon 按钮](/create-a-buy-on-amazon-button-for-shopify-store/buy-now-on-amazon-button.png)

接下来，打开我们 Shopify 独立站的后台，点击左下角的**设置 (Settings)** 按钮，然后在左侧的菜单中选择**文件 (Files)**，再点击右上角的上传文件按钮，将我们刚才下载的图片上传至 Shopify 后台。上传完成后，我们还需要点击图片右侧的链接图标复制图片链接，可以先将该链接粘贴到一个文本文档中，稍后我们会用到。

![将图片上传至 Shopify 独立站](/create-a-buy-on-amazon-button-for-shopify-store/upload-image-to-shopify-store.png)

## 二、编辑 Shopify 主题产品页的代码

回到 Shopify 独立站的后台，依次点击**在线商店 > 模版 > 编辑 > 编辑代码**，打开 Shopify 主题的代码管理页面。

![Shopify 独立站后台编辑代码](/create-a-buy-on-amazon-button-for-shopify-store/shopify-store-edit-code.png)

在搜索框中输入 `product` 然后在 **Sections** 下方点击 `main-product.liquid` 这个文件，右侧会显示该文件包含的具体代码。我们点击右侧的代码区域，使其显示光标 (即我们在输入文字时一闪一闪的那条竖线)，然后使用 Windows 的快捷键 Ctrl + F 或 Mac 的快捷键 command + F 进行搜索，搜索的内容一般为 `add_to_cart`。

{% note warning flat %}
该教程使用的是 Shopify 默认的 Dawn 主题，如果你使用的是其他主题，则可能是 **Sections** 或者 **Snippets** 下方的 “**product-form.liquid**” 或者 “**product-template.liquid**” 文件。另外搜索 **add_to_cart** 如果搜不到，也可以尝试搜索 **add to cart** 或直接搜索 **cart**。
{% endnote %}

### 1. 在 Add to Cart 按钮下方添加图片形式按钮

在下图所示的位置添加我们下方提供的代码，代码第二行中的 `图片链接` 要记得替换为我们在第一步中上传图片后复制的那个链接。

![搜索 add_to_cart 并添加代码](/create-a-buy-on-amazon-button-for-shopify-store/search-add-to-cart.png)

```html
<a href={{ product.variants.first.barcode }} target="_blank">
  <img width="100%" src="图片链接">
</a>
```

其中：

- `href={{ product.variants.first.barcode }}` 表示该按钮的打开链接为产品编辑页面库存部分的**条码 (Barcode)** 中输入的内容，我们只需在每个产品编辑页面的**条码 (Barcode)** 中输入该产品所对应的亚马逊产品链接即可，如下图所示。如果你不想占用**条码 (Barcode)** 而想使用 **SKU**，就把这部分代码中的 `barcode` 替换为 `sku` 即可，不过用户在我们 Shopify 独立站下单后收到的订单确认邮件是会显示 SKU 的，所以尽量不要用 SKU 的位置来输入亚马逊的产品链接。

  ![在条码处输入对应的亚马逊产品链接](/create-a-buy-on-amazon-button-for-shopify-store/shopify-product-barcode.png)

- `target="_blank"` 表示当用户点击 Buy on Amazon 的按钮后，会将亚马逊对应的产品链接在新的标签页中打开，如果你希望顾客点击 Buy on Amazon 的按钮后直接打开亚马逊对应的产品链接而覆盖掉当前 Shopify 的产品页面，可以将这部分代码删除。
- `width="100%"` 是为了限制按钮图片的宽度，一般来说设置为 100% 是刚好可以和其他的按钮保持宽度一致的。
- `src="图片链接"` 表示按钮图片的链接，我们需要将 `图片链接` 替换为第一步中上传图片后复制的那个链接。

### 2. 在动态结账 (Buy It Now) 按钮下方添加图片形式按钮

如果你想把 **Buy on Amazon** 的按钮放在动态结账 (Buy It Now) 按钮的下方，则需要先在第二行代码的 `width="100%"` 之后再插入 `style="margin-top: 10px;"` 这段代码，即完整的代码如下所示。

```html
<a href={{ product.variants.first.barcode }} target="_blank">
  <img width="100%" style="margin-top: 10px;" src="图片链接">
</a>
```

这是为了将 Buy on Amazon 按钮与动态结账按钮之间的间距调整为 10px，因为实测过程中发现这两个按钮之间是没有间距的。如果你觉得间距太大或太小，可以将 10 改成其他的数字，调整到满意为止。

然后再将新的代码移动到下图所示的位置即可。

![将图片形式按钮的代码放在动态结账按钮后](/create-a-buy-on-amazon-button-for-shopify-store/image-button-code-after-dynamic-checkout-button.png)

这样在我们 Shopify 独立站产品详情页就会出现图片形式的 **Buy on Amazon** 按钮了，具体效果如下图所示。点击该按钮后，就会在新的标签页中打开我们对应的亚马逊产品链接了。这里我们选择的按钮图片有点太大了，在实际操作过程中，我们可以让美工根据原按钮的比例自己制作一张合适的图片来替换即可。

![图片形式按钮的实际效果](/create-a-buy-on-amazon-button-for-shopify-store/final-result-of-image-button.png)

### 3. 在 Add to Cart 按钮下方添加文字形式按钮

如果你不想用图片形式的按钮，也可以在下图所示的位置添加我们提供的另一种代码来将 **Buy on Amazon** 按钮改成文字形式，放在 Add to Cart 按钮的下方。

![将文字形式按钮的代码放在 Add to Cart 后](/create-a-buy-on-amazon-button-for-shopify-store/text-button-code-after-add-to-cart-button.png)

```html
<a class="product-form__submit button button--full-width" href="{{ product.variants.first.barcode }}" target="_blank" style="margin-top: 10px;">Buy on Amazon</a>
```

其中：

- `class="product-form__submit button button--full-width"` 表示该按钮的样式，我们只需将自己所用主题下的 Add to Cart 按钮的样式复制过来用即可，如下图所示。

  ![Add to Cart 按钮的 CSS 样式](/create-a-buy-on-amazon-button-for-shopify-store/css-of-add-to-cart-button.png)

- `href="{{ product.variants.first.barcode }}"` 表示该按钮的打开链接为产品编辑页面库存部分的**条码 (Barcode)** 中输入的内容，我们只需在每个产品编辑页面的**条码 (Barcode)** 中输入该产品所对应的亚马逊产品链接即可，如下图所示。如果你不想占用**条码 (Barcode)** 而想使用 **SKU**，就把这部分代码中的 `barcode` 替换为 `sku` 即可，不过用户在我们 Shopify 独立站下单后收到的订单确认邮件是会显示 SKU 的，所以尽量不要用 SKU 的位置来输入亚马逊的产品链接。

  ![在条码处输入对应的亚马逊产品链接](/create-a-buy-on-amazon-button-for-shopify-store/shopify-product-barcode.png)

- `target="_blank"` 表示当用户点击 Buy on Amazon 的按钮后，会将亚马逊对应的产品链接在新的标签页中打开，如果你希望顾客点击 Buy on Amazon 的按钮后直接打开亚马逊对应的产品链接而覆盖掉当前 Shopify 的产品页面，可以将这部分代码删除。

- `style="margin-top: 10px;"` 表示 Buy on Amazon 这个按钮与上一个按钮之间的间距为 10px，如果你觉得间距太大或太小，可以将 10 改成其他的数字，调整到满意为止。

### 4. 在动态结账 (Buy It Now) 按钮下方添加文字形式按钮

如果你想将 **Buy on Amazon** 按钮放在动态结账 (Buy It Now) 按钮下方，只需将代码移动到下图所示的位置即可。

![将文字形式按钮的代码放在动态结账按钮后](/create-a-buy-on-amazon-button-for-shopify-store/text-button-code-after-dynamic-checkout-button.png)

这样在我们 Shopify 独立站产品详情页就会出现文字形式的 **Buy on Amazon** 按钮了，具体效果如下图所示。点击该按钮后，就会在新的标签页中打开我们对应的亚马逊产品链接了。

![文字形式按钮的最终效果](/create-a-buy-on-amazon-button-for-shopify-store/final-result-of-text-button.png)

## 三、补充

由于不同的 Shopify 主题是由不同的开发者开发的，其代码结构千差万别，因此在设置过程中可能会遇到困难。此外，有些朋友的独立站可能需要投放谷歌购物广告，可能无法在条码 (Barcode) 处输入亚马逊产品链接，如果安装第三方插件则担心会拖慢自己 Shopify 独立站的速度，因此需要一个更好的解决方案。如果你遇到类似的问题，可以通过邮箱 `b2cstory@gmail.com` 与我们联系，我们有现成的解决方案，可以实现不占用 SKU 和 Barcode 的位置来实现 Shopify 独立站的产品和亚马逊店铺的产品一一对应。

如果你觉得本站的内容对你有所帮助，欢迎分享给你身边做 Shopify 独立站的朋友来帮助到更多的人。
