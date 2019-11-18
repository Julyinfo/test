---
description: 區分內容資訊功能。
---

# 頁籤 Page Label

使用頁籤可將類似資訊在同頁顯示，不必等待轉頁時間，對於使用者體驗更加友善。

以「會員資料檢視」做為範例：

![](../.gitbook/assets/page_label.png)

![](../.gitbook/assets/label_image_02.png)

以下為兩種狀態示意：

![](../.gitbook/assets/label_image.png)

以下為上方示意圖參考html/css代碼：

```markup
<div class="range">
  <div class="grids hold">相關資料</div>
  <div class="grids">其他資訊</div>
  <div class="grids">專利代理人</div>
  <div class="grids">同意書</div>
  <a href="6-2-2_change_password.html" class="grids">修改密碼</a>
</div>
```

```css
/*--預設樣式--*/
.reviewclass{ font-size:0; margin-bottom:10px; }
.reviewclass .grids{ display: inline-block; vertical-align: middle; margin: 0 10px 0 0; color: #333; font-size: 18px; line-height: 40px; padding: 0 20px; background: #eee; border-radius: 5px; -webkit-border-radius: 5px; -moz-border-radius: 5px; text-decoration: none; cursor: pointer; }
/*--目前樣式--*/
.reviewclass .grids.hold{ background:#2fa4db; color:#fff; }
```

