# 按鈕 Button

## 「進入」或「下一步」用按鈕

![](../.gitbook/assets/buttom_image_01.png)

{% hint style="warning" %}
滑鼠反應只在電腦版本當中會出現，在行動裝置瀏覽時不會出現滑鼠反應。
{% endhint %}

```css
/*--預設樣式--*/
.button{ height:42px; line-height:42px; background-color:#005798; padding:0 20px; font-size:18px; color:#fff; transition:.2s;}

/*--反應樣式--*/
.button:hover{ background-color:#0c6eb7; transition:.2s;}
```

## 「外部連結」用按鈕

![](../.gitbook/assets/buttom_image_02.png)

以下為上方示意圖之html/css代碼：

```markup
<div class="ready_one_link">
  <a class="outLink" href="1-1-2_checksum.html">按鈕文字<i class="fa fa-arrow-right" aria-hidden="true"></i></a>
  <p class="outLinkTxt">按鈕文字輔助說明文案</p>
</div>
```

```css
.ready_one_link{ padding:0 10px; display:inline-block; vertical-align:top;}
.outLink{padding:0 10px; line-height:31px; border:2px solid #0068b7; color:#0068b7; font-weight:500; box-shadow:0 3px 7px 0 rgba(0,0,0,.15);}
.outLink i{ width:25px; height:35px; line-height:31px; color:#0068b7; position:absolute; top:0; right:0; font-size:20px;}
.ready_one_link .outLinkTxt{ font-size:14px; color:#0068b7;}
```

