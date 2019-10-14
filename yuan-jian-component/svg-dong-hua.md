---
description: 在頁面讀取完畢時，於Loading畫面結束，以程式載入SVG檔案，並線性畫出SVG檔案。
---

# SVG動畫

### 程式結構

程式結構如下方範例，

需由`<div>`包覆SVG顯示的區域，於`<div>`加上`id`元素，此`id`需為唯一`id`，

並於內容加上IE版本判斷設定，

IE8至以下為`<!--[if lte IE 8]>ie8至以下顯示內容<![endif]-->`所示；

其他瀏覽器及IE9至以上版本為`<!--[if !IE|gte IE 9]>ie9至以上及其他瀏覽器<!--><!--<![endif]-->`。

```markup
<div id="SVG_ID">
  <!--[if lte IE 8]>
  <img src="替代圖片位置">
  <![endif]-->
  <!--[if !IE|gte IE 9]><!-->
  <script>svgTimeout( 'SVG_ID', 'SVG檔案相對位置' );</script>
  <!--<![endif]-->
</div>
```

其他瀏覽器及IE9至以上版本則可放入SVG動畫執行程式`<script>vgTimeout('SVG_ID', 'SVG檔案相對位置');</script>`，程式將自動載入`SVG檔案相對位置`的SVG檔案至`SVG_ID`的`<div>`中，並於loading畫面結束後，執行SVG動畫。



