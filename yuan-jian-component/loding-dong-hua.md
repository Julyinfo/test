# 載入動畫 Loding

![](../.gitbook/assets/loading_low_ie.jpg)

![](../.gitbook/assets/loading.jpg)

電腦版CSS

```css
.loading_box{ width:100%; height:100%; position:fixed; top:0; left:0; z-index:9999; background-color:#ffffff;}
.loading_line{ width:600px; height:140px; margin:auto; position:relative; overflow:hidden; top:50%; margin:-50px auto 0 auto; left:0; right:0;}
.loading_line.low_ie{ width:100px; }
.loading_image{ width:100px; height:100px; display:inline-block; background:url(../images/layout/loading.jpg) no-repeat top left; animation:loadingimage01 2s steps(23) infinite; position:absolute; top:0; animation-delay:-2s; z-index:6;}
.loading_image_low_ie { width:100px; height:100px; display:inline-block; background:url(../images/layout/loading_low_ie.jpg) no-repeat top left; position:absolute; top:0; left:0; z-index:6; }
.loading_image:nth-child(2){ animation-delay:-1.6s; z-index:5;}
.loading_image:nth-child(3){ animation-delay:-1.2s; z-index:4;}
.loading_image:nth-child(4){ animation-delay:-0.8s; z-index:3;}
.loading_image:nth-child(5){ animation-delay:-0.4s; z-index:2;}
.loading_image:nth-child(6){ animation-delay:0s; z-index:1;}
@keyframes loadingimage01{ 0%{ background-position-x:0px; left:0px;} 100%{ background-position-x:-2300px; left:500px;}}
@keyframes loadingimage02{ 0%{ background-position-x:0px; left:0px;} 100%{ background-position-x:-2300px; left:500px;}}
@keyframes loadingimage03{ 0%{ background-position-x:0px; left:0px;} 100%{ background-position-x:-2300px; left:500px;}}
@keyframes loadingimage04{ 0%{ background-position-x:0px; left:0px;} 100%{ background-position-x:-2300px; left:500px;}}
@keyframes loadingimage05{ 0%{ background-position-x:0px; left:0px;} 100%{ background-position-x:-2300px; left:500px;}}
@keyframes loadingimage06{ 0%{ background-position-x:0px; left:0px;} 100%{ background-position-x:-2300px; left:500px;}}
.loading_text{ font-size:16px; line-height:30px; color:#ccc; text-align:center; padding-top:110px;}
```

手機版CSS

```css
@media screen and (max-width:767px){
.loading_line{ width:250px; height:120px;}
.loading_image{ width:50px; height:50px; background-size:1150px 50px;}
.loading_text{ padding-top:70px; font-size:25px;}
@keyframes loadingimage01{ 0%{ background-position-x:0px; left:0px;} 100%{ background-position-x:-1150px; left:250px;}}
@keyframes loadingimage02{ 0%{ background-position-x:0px; left:0px;} 100%{ background-position-x:-1150px; left:250px;}}
@keyframes loadingimage03{ 0%{ background-position-x:0px; left:0px;} 100%{ background-position-x:-1150px; left:250px;}}
@keyframes loadingimage04{ 0%{ background-position-x:0px; left:0px;} 100%{ background-position-x:-1150px; left:250px;}}
@keyframes loadingimage05{ 0%{ background-position-x:0px; left:0px;} 100%{ background-position-x:-1150px; left:250px;}}
@keyframes loadingimage06{ 0%{ background-position-x:0px; left:0px;} 100%{ background-position-x:-1150px; left:250px;}}
}
```

在中載入 jquery檔案，於jquery後方加入以下&lt;script&gt;。

```javascript
<script type="text/javascript" src="scripts/page_scripts.js"></script>
```

動畫會在頁面讀取完畢後結束Loading動畫

