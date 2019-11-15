# 狀態 Status

服務狀態會以三種顏色來區分出不同的狀態，使用不同的顏色來便於使用者能夠輕易辨識，欲使用的項目是否正常執行服務中。其中會以正常、維護、異常，三種狀態來提供辨識，以下為三種狀態介紹：

| 服務狀態 | 狀態說明 |
| :--- | :--- |
| ![](../.gitbook/assets/color_02.png)正常服務中 | 目前所有功能均正常提供服務。 |
| ![](../.gitbook/assets/color_03.png)維護服務中 | 目前正在更新、維修或系統相關調整作業。 |
| ![](../.gitbook/assets/color_04.png)異常服務中 | 目前服務異常並暫時無法使用。 |

## 正常服務中

![](../.gitbook/assets/status_image_01.jpg)

目前所有功能均正常提供服務。

* 狀態顏色：\#41D4B3
* 齒輪狀態：持續旋轉 \(單圈/5s\)
* 顯示文字：正常
* 動態動畫：有

以下為動畫html/css代碼：

```markup
<a href="#" class="bgs">
  <div class="ranges">
    <div class="icons"><i class="fa fa-cog" aria-hidden="true"></i></div>
    <div class="names">電子送件</div>
    <div class="current">正常</div>
    <i class="fa fa-angle-right" aria-hidden="true"></i>
  </div>
  <div class="mvbg">
    <svg class="waves" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" viewBox="0 24 150 28" preserveAspectRatio="none" shape-rendering="auto">
      <defs>
        <path id="gentle-wave" d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z"></path>
      </defs>
      <g class="parallax">
        <use xlink:href="#gentle-wave" x="48" y="0" fill="rgba(65,212,73,0.2)"></use>
        <use xlink:href="#gentle-wave" x="48" y="3" fill="rgba(65,212,73,0.3)"></use>
        <use xlink:href="#gentle-wave" x="48" y="5" fill="rgba(65,212,73,0.4)"></use>
        <use xlink:href="#gentle-wave" x="48" y="7" fill="#fff"></use>
      </g>
    </svg>
  </div>
</a>
```

```css
/*維護計畫*/
.maintain{ margin:0 0 60px 0; padding:45px 0 30px 0; border-bottom:1px solid #ccc; }
.maintain .mar{ max-width:1280px; padding:0 40px; margin:auto; }
.status{ margin-left:-20px; font-size:0; }
.status .grids{ width:33.333%; display:inline-block; vertical-align:top; padding-left:20px; }
.status .grids .bgs{ display:block; width:100%; background:#fff; border:1px solid #41d449; line-height:60px; overflow:hidden; border-radius:5px; -webkit-border-radius:5px; -moz-border-radius:5px; position:relative; text-decoration:none;}
/*.status .grids .bgs:after{ content:""; display:block; width:14px; height:14px; border-top:2px solid #fff; border-right:2px solid #fff; position:absolute; right:20px; top:50%; margin-top:-8px; transform:rotate(45deg); -webkit-transform:rotate(45deg); -moz-transform:rotate(45deg); }*/
.status .grids .bgs::after{ content:""; display:block;}
.status .grids .bgs .fa-angle-right{ font-size: 38px; color: #41d449; position: absolute; right: 0px; top: -2px; line-height:60px; height:60px; padding-right:15px;}
.status .grids .bgs .icons{ display:inline-block; vertical-align:middle; font-size:36px; color:#fff; background-color: #41d449; height:60px; width:60px; line-height:60px; vertical-align:middle; text-align:center; }
.status .grids .bgs .icons i{ line-height:60px; animation:5s deg linear infinite; -webkit-animation:5s deg linear infinite; -moz-animation:5s deg linear infinite;}
@keyframes deg{0%{ transform:rotate(0deg); -webkit-transform:rotate(0deg); -moz-transform:rotate(0deg); }
100%{ transform:rotate(360deg); -webkit-transform:rotate(360deg); -moz-transform:rotate(360deg); }}
0%{ transform:rotate(0deg); -webkit-transform:rotate(0deg); -moz-transform:rotate(0deg); }
@-webkit-keyframes deg{100%{ transform:rotate(360deg); -webkit-transform:rotate(360deg); -moz-transform:rotate(360deg); }}
@-moz-keyframes deg{0%{ transform:rotate(0deg); -webkit-transform:rotate(0deg); -moz-transform:rotate(0deg); }
100%{ transform:rotate(360deg); -webkit-transform:rotate(360deg); -moz-transform:rotate(360deg); }}

.status .grids .bgs .names{ display:inline-block; vertical-align:middle; font-size:25px; color:#41d449; padding-left:15px; }
.status .grids .bgs .current{ display:inline-block; vertical-align:middle; font-size:25px; color:#41d449; font-weight:bold; padding-left:15px; }

.status .grids .bgs .ranges{ position:relative; z-index:5; }
.status .grids .bgs .mvbg{ position:absolute; top:0; left:0; right:0; bottom:0; margin:auto; transform:rotate(180deg); -webkit-transform:rotate(180deg); -moz-transform:rotate(180deg); }

.statusBox{ padding:30px 0 0 0; }
.statusBox .stitle{ font-size:25px; color:#333; font-weight:bold; margin:0 0 15px 0; }
.statusBox .slist{ display:block; text-decoration:none; border-top:1px solid #ddd; padding:15px 0; }
.statusBox .slist .date{ padding:0 0 5px 0; }
.statusBox .slist .date .s1{ display:inline-block; vertical-align:middle; background:#ec5b5e; border-radius:3px; -webkit-border-radius:3px; -moz-border-radius:3px; padding:2px 4px; color:#fff; font-size:14px; }
.statusBox .slist .date .s2{ display:inline-block; vertical-align:middle; font-size:14px; color:#999; }
.statusBox .slist .vtitle{ font-size:16px; color:#333; }

.status .grids.error .bgs{/* background:#f7d5d5; border-left:10px solid #e86a6a;*/ border:1px solid #e25757;}
.status .grids.error .bgs .icons{ background-color:#e25757;}
.status .grids.error .bgs .names{ color:#e25757;}
.status .grids.error .bgs .current{ color:#e25757;}
.status .grids.error .bgs .fa-angle-right{ color:#e25757;}
.status .grids.error .bgs .icons i{ animation:noen; -webkit-animation:none; -moz-animation:noen;}
.status .grids.repair .bgs{/* background:#fdf2d0; border-left:10px solid #f0c74a;*/ border:1px solid #f0a34a;}
.status .grids.repair .bgs .icons{ background-color:#f0a34a;}
.status .grids.repair .bgs .names{ color:#f0a34a;}
.status .grids.repair .bgs .current{ color:#f0a34a;}
.status .grids.repair .bgs .fa-angle-right{ color:#f0a34a;}
.status .grids.repair .bgs .icons i{ animation:noen; -webkit-animation:none; -moz-animation:noen;}

.status .grids.error .waves{ padding-top:50px; }
.status .grids.repair .waves{ padding-top:50px; }
.status .grids.error .bgs .icons{ animation:none; -webkit-animation:none; -moz-animation:none; }
.status .grids.repair .bgs .icons{ animation:none; -webkit-animation:none; -moz-animation:none; }

/*小動畫*/
.waves { position: relative;
        width: 100%;
        height: 15vh;
        margin-bottom: -7px; /*Fix for safari gap*/
		height:61px;
		padding-top:20px;
        }
```

## 維護服務中

![](../.gitbook/assets/status_image_02.jpg)

目前正在更新、維修或系統相關調整作業。

* 狀態顏色：\#F0C74A
* 齒輪狀態：停止
* 顯示文字：維護中
* 動態動畫：無

```markup
<a href="#" class="bgs">
  <div class="ranges">
    <div class="icons"><i class="fa fa-cog" aria-hidden="true"></i></div>
    <div class="names">電子送達</div>
    <div class="current">維護中</div>
    <i class="fa fa-angle-right" aria-hidden="true"></i>
  </div>
</a>
```

## 異常服務中

![](../.gitbook/assets/status_image_03.jpg)

目前服務異常並暫時無法使用。

* 狀態顏色：\#E86A6A
* 齒輪狀態：停止
* 顯示文字：維護中
* 動態動畫：無

