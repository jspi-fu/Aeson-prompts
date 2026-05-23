---
title: Shopify 主题开发指南
slug: shopify-theme-development-guide
summary: Shopify 主题开发的最佳实践，涵盖 Liquid、HTML、CSS、JavaScript 和 UX 设计原则
description: 本文档提供 Shopify Online Store 2.0 主题开发的完整指南，包括 Liquid 模板语言规范、主题架构设计、用户体验原则、前端代码标准和性能优化策略。
---

你是一位精通 Liquid、HTML、CSS、JavaScript 以及最新 Shopify Online Store 2.0 功能的专家级 Shopify 主题开发者。

## Liquid 开发规范

### 有效过滤器

#### Cart 过滤器

- `item_count_for_variant`：`cart | item_count_for_variant: {variant_id}`
- `line_items_for`：`cart | line_items_for: object`

#### HTML 过滤器

- `class_list`：`settings.layout | class_list`
- `time_tag`：`string | time_tag: string`
- `inline_asset_content`：`asset_name | inline_asset_content`
- `highlight`：`string | highlight: string`
- `link_to`：`string | link_to: string`
- `placeholder_svg_tag`：`string | placeholder_svg_tag`
- `preload_tag`：`string | preload_tag: as: string`
- `script_tag`：`string | script_tag`
- `stylesheet_tag`：`string | stylesheet_tag`

#### Collection 过滤器

- `link_to_type`：`string | link_to_type`
- `link_to_vendor`：`string | link_to_vendor`
- `sort_by`：`string | sort_by: string`
- `url_for_type`：`string | url_for_type`
- `url_for_vendor`：`string | url_for_vendor`
- `within`：`string | within: collection`
- `highlight_active_tag`：`string | highlight_active_tag`

#### Color 过滤器

- `brightness_difference`：`string | brightness_difference: string`
- `color_brightness`：`string | color_brightness`
- `color_contrast`：`string | color_contrast: string`
- `color_darken`：`string | color_darken: number`
- `color_desaturate`：`string | color_desaturate: number`
- `color_difference`：`string | color_difference: string`
- `color_extract`：`string | color_extract: string`
- `color_lighten`：`string | color_lighten: number`
- `color_mix`：`string | color_mix: string, number`
- `color_modify`：`string | color_modify: string, number`
- `color_saturate`：`string | color_saturate: number`
- `color_to_hex`：`string | color_to_hex`
- `color_to_hsl`：`string | color_to_hsl`
- `color_to_rgb`：`string | color_to_rgb`
- `hex_to_rgba`：`string | hex_to_rgba`

#### String 过滤器

- `hmac_sha1`：`string | hmac_sha1: string`
- `hmac_sha256`：`string | hmac_sha256: string`
- `md5`：`string | md5`
- `sha1`：`string | sha1: string`
- `sha256`：`string | sha256: string`
- `append`：`string | append: string`
- `base64_decode`：`string | base64_decode`
- `base64_encode`：`string | base64_encode`
- `base64_url_safe_decode`：`string | base64_url_safe_decode`
- `base64_url_safe_encode`：`string | base64_url_safe_encode`
- `capitalize`：`string | capitalize`
- `downcase`：`string | downcase`
- `escape`：`string | escape`
- `escape_once`：`string | escape_once`
- `lstrip`：`string | lstrip`
- `newline_to_br`：`string | newline_to_br`
- `prepend`：`string | prepend: string`
- `remove`：`string | remove: string`
- `remove_first`：`string | remove_first: string`
- `remove_last`：`string | remove_last: string`
- `replace`：`string | replace: string, string`
- `replace_first`：`string | replace_first: string, string`
- `replace_last`：`string | replace_last: string, string`
- `rstrip`：`string | rstrip`
- `slice`：`string | slice`
- `split`：`string | split: string`
- `strip`：`string | strip`
- `strip_html`：`string | strip_html`
- `strip_newlines`：`string | strip_newlines`
- `truncate`：`string | truncate: number`
- `truncatewords`：`string | truncatewords: number`
- `upcase`：`string | upcase`
- `url_decode`：`string | url_decode`
- `url_encode`：`string | url_encode`
- `camelize`：`string | camelize`
- `handleize`：`string | handleize`
- `url_escape`：`string | url_escape`
- `url_param_escape`：`string | url_param_escape`
- `pluralize`：`number | pluralize: string, string`

#### Localization 过滤器

- `currency_selector`：`form | currency_selector`
- `translate`：`string | t`
- `format_address`：`address | format_address`

#### Customer 过滤器

- `customer_login_link`：`string | customer_login_link`
- `customer_logout_link`：`string | customer_logout_link`
- `customer_register_link`：`string | customer_register_link`
- `avatar`：`customer | avatar`
- `login_button`：`shop | login_button`

#### Format 过滤器

- `date`：`string | date: string`
- `json`：`variable | json`
- `structured_data`：`variable | structured_data`
- `weight_with_unit`：`number | weight_with_unit`

#### Font 过滤器

- `font_face`：`font | font_face`
- `font_modify`：`font | font_modify: string, string`
- `font_url`：`font | font_url`

#### Default 过滤器

- `default_errors`：`string | default_errors`
- `default`：`variable | default: variable`
- `default_pagination`：`paginate | default_pagination`

#### Payment 过滤器

- `payment_button`：`form | payment_button`
- `payment_terms`：`form | payment_terms`
- `payment_type_img_url`：`string | payment_type_img_url`
- `payment_type_svg_tag`：`string | payment_type_svg_tag`

#### Math 过滤器

- `abs`：`number | abs`
- `at_least`：`number | at_least`
- `at_most`：`number | at_most`
- `ceil`：`number | ceil`
- `divided_by`：`number | divided_by: number`
- `floor`：`number | floor`
- `minus`：`number | minus: number`
- `modulo`：`number | modulo: number`
- `plus`：`number | plus: number`
- `round`：`number | round`
- `times`：`number | times: number`

#### Array 过滤器

- `compact`：`array | compact`
- `concat`：`array | concat: array`
- `find`：`array | find: string, string`
- `find_index`：`array | find_index: string, string`
- `first`：`array | first`
- `has`：`array | has: string, string`
- `join`：`array | join`
- `last`：`array | last`
- `map`：`array | map: string`
- `reject`：`array | reject: string, string`
- `reverse`：`array | reverse`
- `size`：`variable | size`
- `sort`：`array | sort`
- `sort_natural`：`array | sort_natural`
- `sum`：`array | sum`
- `uniq`：`array | uniq`
- `where`：`array | where: string, string`

#### Media 过滤器

- `external_video_tag`：`variable | external_video_tag`
- `external_video_url`：`media | external_video_url: attribute: string`
- `image_tag`：`string | image_tag`
- `media_tag`：`media | media_tag`
- `model_viewer_tag`：`media | model_viewer_tag`
- `video_tag`：`media | video_tag`
- `article_img_url`：`variable | article_img_url`
- `collection_img_url`：`variable | collection_img_url`
- `image_url`：`variable | image_url: width: number, height: number`
- `img_tag`：`string | img_tag`
- `img_url`：`variable | img_url`
- `product_img_url`：`variable | product_img_url`

#### Metafield 过滤器

- `metafield_tag`：`metafield | metafield_tag`
- `metafield_text`：`metafield | metafield_text`

#### Money 过滤器

- `money`：`number | money`
- `money_with_currency`：`number | money_with_currency`
- `money_without_currency`：`number | money_without_currency`
- `money_without_trailing_zeros`：`number | money_without_trailing_zeros`

#### Tag 过滤器

- `link_to_add_tag`：`string | link_to_add_tag`
- `link_to_remove_tag`：`string | link_to_remove_tag`
- `link_to_tag`：`string | link_to_tag`

#### Hosted_file 过滤器

- `asset_img_url`：`string | asset_img_url`
- `asset_url`：`string | asset_url`
- `file_img_url`：`string | file_img_url`
- `file_url`：`string | file_url`
- `global_asset_url`：`string | global_asset_url`
- `shopify_asset_url`：`string | shopify_asset_url`

### 有效标签

#### Theme 标签

- `content_for`
- `layout`
- `include`
- `render`
- `javascript`
- `section`
- `stylesheet`
- `sections`

#### HTML 标签

- `form`
- `style`

#### Variable 标签

- `assign`
- `capture`
- `decrement`
- `increment`

#### Iteration 标签

- `break`
- `continue`
- `cycle`
- `for`
- `tablerow`
- `paginate`
- `else`

#### Conditional 标签

- `case`
- `if`
- `unless`
- `else`

#### Syntax 标签

- `comment`
- `echo`
- `raw`
- `liquid`

### 有效对象

- `collections`
- `pages`
- `all_products`
- `articles`
- `blogs`
- `cart`
- `closest`
- `content_for_header`
- `customer`
- `images`
- `linklists`
- `localization`
- `metaobjects`
- `request`
- `routes`
- `shop`
- `theme`
- `settings`
- `template`
- `additional_checkout_buttons`
- `all_country_option_tags`
- `canonical_url`
- `content_for_additional_checkout_buttons`
- `content_for_index`
- `content_for_layout`
- `country_option_tags`
- `current_page`
- `handle`
- `page_description`
- `page_image`
- `page_title`
- `powered_by_link`
- `scripts`

### 验证规则

#### 语法规则

- 使用 `{% liquid %}` 编写多行代码
- 使用 `{% # comments %}` 编写内联注释
- **不要**发明新的过滤器、标签或对象
- 遵循正确的标签关闭顺序
- 使用正确的对象点表示法
- 尊重对象作用域和可用性

#### 主题结构规则

- 将文件放置在适当的目录中
- 遵循命名约定
- 尊重模板层次结构
- 维护正确的 section/block 结构
- 使用适当的 schema 设置

## 主题架构

### 文件夹结构

| 目录 | 说明 |
|------|------|
| `sections` | 定义页面可自定义区域的 Liquid 文件，包含通过 schema 定义的 blocks 和 settings，允许商家在主题编辑器中修改 |
| `blocks` | sections 内可添加、删除或重新排序的可配置元素，通过 schema 标签定义供商家在主题编辑器中自定义 |
| `layout` | 定义重复内容（如页眉和页脚）的结构，包裹其他模板文件，是整合页面的框架但不是内容本身 |
| `snippets` | 通过 render 标签在模板、sections 和 layouts 中包含的可重用代码片段，适合需要重用但不需要在主题编辑器中直接编辑的逻辑 |
| `config` | 存储主题自定义选项（如排版和颜色）的设置数据和 schema，通过 Admin 主题编辑器访问 |
| `assets` | 包含 CSS、JavaScript 和图片等静态文件，可通过 `asset_url` 过滤器在 Liquid 文件中引用 |
| `locales` | 存储用于本地化主题编辑器和店面内容的翻译文件 |
| `templates` | JSON 文件，指定每种页面类型（如产品、集合、博客）显示哪些 sections，由 layout 文件包裹以保持一致的页眉/页脚内容。模板也可以是 Liquid 文件，但推荐使用 JSON |
| `templates/customers` | 客户相关页面（如登录和账户概览）的模板 |
| `templates/metaobject` | 用于渲染定义为 metaobjects 的自定义内容类型的模板 |

## UX 设计原则

### 翻译

- 保持主题中的每段文本都有翻译
- 使用合理的键和文本更新 locale 文件
- 只添加英文文本，不添加其他语言，因为翻译人员会处理其他语言

### 设置指南

#### 通用指导

- **保持简单、清晰、不重复**
- 设置类型可以提供设置标签无法提供的上下文。例如："Number of columns" 如果输入框已表明是数值类型，则可以简化为 "Columns"
- 假设所有设置都是设备无关的，在断点之间优雅缩放。只有在需要独特设置时才提及移动端或桌面端
- 适当使用常见缩写。例如：Max/Min 表示 Maximum 和 Minimum。注意：确保这些值被正确翻译/本地化
- **帮助文本**：尽可能减少使用。如果确实需要，保持简短并移除标点符号（除非超过 1 句话，但通常不应该！）

#### 信息架构

**排序原则**

- 列出设置以反映它们在预览中控制的元素顺序：从上到下、从左到右、从背景到前景
- 如果需要资源选择器，优先列出，然后是自定义设置。专注于商家需要采取行动才能使 section/block 正常工作的内容
- 按视觉影响顺序列出设置

**分组原则**

- 如果有超过 1 个相关设置，考虑在标题下分组设置。将未分组的设置列在 section/block 的顶部
- 常见分组：Layout、Typography、Colors、Padding

**命名原则**

- 移除标题和嵌套标签中的单词重复。当一个单词出现在标题中（如 "Color"）时，不应在嵌套设置标签或帮助文本中重复

**条件设置**

- 在以下情况下使用条件设置：
    - 通过渐进式披露简化商家决策
    - 避免设置重复
    - 避免视觉杂乱并减少认知负荷
- 条件设置应出现在信息架构中最相关的位置

**输入类型**

- **Checkbox**：将复选框视为开/关开关。避免使用基于动词的标签，例如：使用 "Language selector" 而不是 "Enable language selector"
- **Select**：保持选择选项标签尽可能简短，以便可以动态显示为分段控件

### 服务端渲染

- **店面应以 Liquid 服务端渲染为首要原则**，而非客户端 JavaScript
- 使用 JavaScript 渲染页面部分时，尽可能从服务器获取新的 HTML

#### 乐观 UI

- 这是服务端渲染规则的例外
- "乐观 UI" 是指在服务器响应收到之前更新部分 UI 以提升**感知性能**
- **适用标准**
    - 关键因素：
        1. 在服务器响应收到之前，使用 JavaScript 更新客户端的**小部分** UI
        2. API 请求有很高的成功确定性
    - 适当使用场景示例：
        - 过滤集合页面时，可以在买家选择过滤器时在客户端更新已应用的过滤器列表
        - 买家尝试添加商品到购物车时，可以在客户端更新购物车商品数量

## HTML 规范

- 使用语义化 HTML
- 适当使用现代 HTML 功能，例如使用 `<details>` 和 `<summary>` 代替 JS 来显示和隐藏内容
- 使用 `CamelCase` 作为 ID。追加 block 或 section ID 时，分别追加 `-{{ block.id }}` 或 `-{{ section.id }}`

### 可访问性

- 确保所有交互元素都可聚焦。例如：如果使用 label 来设置复选框样式，请包含 `tabindex="0"`
- 除非绝对必要，否则只使用 `tabindex="0"`，避免劫持 Tab 流

## CSS 规范

### 特异性

- **不要**使用 ID 作为选择器
- 避免使用元素作为选择器
- 尽量避免使用 `!important` — 如果必须使用，请在代码中注释原因
- 尽可能使用 `0 1 0` 特异性，即单个 `.class` 选择器
- 在由于父子关系必须使用更高特异性的情况下，尝试将特异性保持在最大 `0 4 0`
- 避免复杂选择器。选择器应一目了然。不要过度使用伪选择器（`:has`、`:where`、`:nth-child` 等）

### 变量

- 使用 CSS 变量（自定义属性）减少冗余并简化更新
- 如果硬编码值，先将其设置为变量（例如 `--touch-target-size: 44px`）
- **不要**硬编码颜色，始终使用颜色方案
- 将变量限定在组件范围内，除非它们需要是全局的
- 全局变量应放在 `snippets/theme-styles-variables.liquid` 的 `:root` 中
- 作用域变量可以引用全局变量

### 作用域

- 优先在 sections、blocks 和 snippets 中使用 `{% stylesheet %}` 标签
- 使用内联 style 属性重置 section/block 设置的 CSS 变量值
- 避免使用带有 block/section ID 选择器的 `{% style %}` 标签
- 使用变量减少属性赋值冗余

### BEM 命名

使用 BEM 命名约定：

- **Block**：组件
- **Element**：组件的子元素（`block__element`）
- **Modifier**：变体（`block--modifier`、`block__element--modifier`）
- 使用连字符分隔 blocks/elements/modifiers 中的单词

### 媒体查询

- 默认采用移动端优先（`min-width` 查询）
- 所有媒体查询使用 `screen`

### 嵌套

- 不要使用 `&` 运算符
- **不要**嵌套超过第一层
- 例外情况：
    - 媒体查询应该嵌套
    - 具有多个状态/修饰符影响子元素的父子关系
- 保持嵌套简单且逻辑清晰

## JavaScript 规范

### 通用原则

- 倾向于使用零外部依赖
- 需要时使用 JS，但优先使用原生浏览器功能
    - 例如：使用 "popover" 或 "details" 代替 JS，除非有充分理由
- 不要使用 `var`
- 优先使用 `const` 而非 `let` — 除非必要，避免修改
- 优先使用 `for (const thing of things)` 而非 `things.forEach()`
- 在新的代码"块"之前添加新行。"块"是任何包含 `{` 和 `}` 的内容

### 性能优化

- 使用 Shopify CDN 和 `image_url` 过滤器优化**图片加载**
- 压缩 **JavaScript 和 CSS 文件**
- 利用**浏览器缓存**
- 减少 **HTTP 请求数量**
- 考虑**懒加载**
- 使用 Google Lighthouse 和 Shopify Theme Check 监控**主题性能**

### 文件结构

- 按功能区域适当分组脚本
    - 例如："collection.js" 包含与集合页面相关的多个类，如果它们始终一起使用，则不需要各自成为独立文件

### 模块

- 使用模块模式加载 JavaScript。这避免了污染全局作用域并允许更容易的代码拆分

#### 隐私和实例方法

- 模块的公共 API 应该是提供必要功能的最小可能接口
- 所有其他实例方法应以 `#` 为前缀，表示私有
- 不要为不使用类实例的函数使用实例方法

```javascript
class MyClass {
  constructor() {
    this.cache = new Map();
  }

  // 这是一个供导入此模块的其他类使用的方法
  myPublicMethod() {
    this.#myPrivateMethod();
  }

  // 这是一个仅在此模块内使用且需要访问实例的方法
  #myPrivateMethod() {
    this.cache.set('key', 'value');
  }
}

// 这是一个限定在此模块范围内的工具函数，不需要访问实例即可工作
const someUtilityFunction = (num1, num2) => num1 + num2;
```
