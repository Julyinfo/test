---
description: 整合站內所有功能，包含了網頁導覽、版權宣告、連絡資訊、行動裝置應用等...。
---

# 頁尾 Footer

![](../.gitbook/assets/footer_banner.png)

### 電腦版與平板

使用**巨型選單** \(Big Footer\) 的方式來呈現，在資訊架構較為複雜多樣的情況下，採用**巨型選單**可以有效陳列出所有的網頁選項，不僅在操作與瀏覽上方便許多，也可以附帶「網站地圖」之展現功能，猶如一個小型的資訊中心。

在最底部安插了「QR Code」之圖像來提供行動裝置掃描，進而提升欲由行動裝置操作瀏覽之使用者的效率瀏覽便利性。

### 手機版

在手機版本取消了選單與 QR Code 的顯示，為了簡化行動裝置的操作與需要思考的動作，選單統一會由「頁首」來提供操作，而 QR Code 在行動裝置並無太大實質效益，進而取消顯示。

![](../.gitbook/assets/footer_image.jpg)

以下為頁尾參考設定值：

```css
footer{ backgroung-color:#eee; padding:40px;}
Lv01_menu{ color:#005798; font-size:16px;}
Lv02_menu{ color:#333; font-size:14px;}
Lv03_menu{ color:#333; font-size:14px;}
footer_button{ background:rgb(0,87,152); background:-moz-linear-gradient(left, rgba(0,87,152,1) 0%, rgba(47,164,219,1) 100%); background:-webkit-linear-gradient(left, rgba(0,87,152,1) 0%,rgba(47,164,219,1) 100%); background:linear-gradient(to right, rgba(0,87,152,1) 0%,rgba(47,164,219,1) 100%);}
footer_buttn_word{ font-size:12px; color:#fff;}
```

以下為頁尾 HTML / CSS ：

{% file src="../.gitbook/assets/footer.html" caption="footer.html - 下載" %}

{% file src="../.gitbook/assets/footer.css" caption="footer.css - 下載" %}

