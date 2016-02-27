title: 客製化我的開發環境並將它開源！
author: PastLeo

%%%%%%%%%%%%%%%%%%%
% Use '%' to comment or directive (ex:css below)

%%%%%%%%%%%%%%%%%%%
%% You can add some custom style rules here...

%css

.many_subtitle h2 {
    margin-top: 15% !important;
}

.step.slogen h2 {
    margin-top: 20%;
}

.step.center-list ul, .step.center-list ul {
    display:table; margin:0 auto;
}

%end

%%%%%%%%%%%%%%%%%%%
%% occupation of scale=1:
%% x = 1200
%% y = 700
%% occupation of scale=2: [occupation of scale=1] * 2
%% x = 2400
%% y = 1400
%% occupation of scale=3: [occupation of scale=1] * 3
%% x = 3600
%% y = 2100
%% occupation of scale=4: [occupation of scale=1] * 4
%% ...
%% the location of one step (slide) is originated from the center!

%%%%%%%%%%%%%%%%%%%
%% Here we go...

%%%%%%%%%%%%%%%
!SLIDE x=0 y=0 slogen

## 客製化我的開發環境並將它開源！

#### PastLeo

%%%%%%%%%%%%%%%
!SLIDE x=0 y=0 z=-2000 many_subtitle slogen

## 我是誰？

#### 一個對環境有強迫症的大四中興同學

#### 名字不重要，因為這是短講，下一張

#### 有興趣的可以去 [http://pastleo.me](http://pastleo.me)

%%%%%%%%%%%%%%%
!SLIDE x=0 y=700 slogen

## 故事是這樣開始的...

%%%%%%%%%%%%%%%
!SLIDE picture x=0 y=700 z=-2000

![Original terminal](http://i.imgur.com/LKZO6IN.png)

#### 這樣誰受的了！？

%%%%%%%%%%%%%%%
!SLIDE picture x=0 y=700 z=-4000

![My terminal](http://i.imgur.com/WfzmmqJ.png)

#### 這樣好多了

%%%%%%%%%%%%%%%
!SLIDE x=0 y=2100 rotate=180 scale=2 slogen

## 你以為我只是寫寫 theme 嗎？

#### 你就大錯特錯了

%%%%%%%%%%%%%%%
!SLIDE x=0 y=1400 z=-1500 rotate=180 slogen

## 強迫症結果一： [dotSetting](https://github.com/chgu82837/dotSetting)

#### 家目錄下的隱藏檔集合，附贈部屬程式

%%%%%%%%%%%%%%%
!SLIDE x=0 y=1400 z=-3000 rotate=180

### Spec

 * 我家目錄的隱藏檔，可以讓我的終端機長得比較炫炮 (廢話)
    * 還包含 `fish` / `vim` 套件自動安裝啥的東西
    * 我自幹的 `fish` 主題：[https://github.com/chgu82837/theme-PastFish](https://github.com/chgu82837/theme-PastFish)
 * 使用 `rsync` 自動佈署
 * 有二層佈署，可以把敏感資料放在第二層 `custom` 資料夾內
 * [https://github.com/chgu82837/dotSetting](https://github.com/chgu82837/dotSetting)

%%%%%%%%%%%%%%%
!SLIDE x=0 y=1400 z=-5000 rotate=180 slogen

## DEMO

#### 安裝一次給大家看

%%%%%%%%%%%%%%%
!SLIDE x=-600 y=2800 z=-1500 rotate=180

## 強迫症結果二： [PastPress](https://github.com/chgu82837/PastPress)

#### 就是你現在看到的簡報的產生器

#### 的 Theme

%%%%%%%%%%%%%%%
!SLIDE x=-600 y=2800 z=-3000 rotate=180

### Spec

 * 基於 [Slideshow s9](http://slideshow-s9.github.io/index.html) 以及 [Impress.js](https://github.com/impress/impress.js)，用 `markdown` 作為簡報撰寫語言
 * 為了解決 `markdown` 撰寫投影片排版的麻煩 (尤其是圖片)，我利用 `slideshow` 可以幫投影片加 `class` 的方式控制圖片排版
 * [https://github.com/chgu82837/PastPress](https://github.com/chgu82837/PastPress)

%%%%%%%%%%%%%%%
!SLIDE x=-600 y=2800 z=-5000 rotate=180 slogen

## DEMO

#### 看一下這個投影片的原始碼囉

%%%%%%%%%%%%%%%
!SLIDE x=600 y=2800 z=-1500 rotate=180

## 強迫症結果三： [dockerRunner](https://github.com/chgu82837/dockerRunner)

#### docker 的小工具

%%%%%%%%%%%%%%%
!SLIDE x=600 y=2800 z=-3000 rotate=180

### Spec

 * 類似 `docker-compose` 可以幫忙下 `docker run` 的設定，但設定可放置在本 git repo 內
    * 這樣就可以在任意資料夾直接執行 `docker image` 一般
 * 另一部分是可以幫忙 `Dockerfile` 的 scaffolding
 * [https://github.com/chgu82837/dockerRunner](https://github.com/chgu82837/dockerRunner)

%%%%%%%%%%%%%%%
!SLIDE x=600 y=2800 z=-5000 rotate=180 slogen

## DEMO

#### 看不懂沒關係，用一次給各位看

%%%%%%%%%%%%%%%
!SLIDE x=0 y=2100 z=-7000 rotate=180 scale=2

## 這三個大概是我目前有開源的客製化小東西

#### 所以你以為要 QA 了嗎？

%%%%%%%%%%%%%%%
!SLIDE x=0 y=4200 scale=3 slogen

## 其實我不是來炫我做了啥的

#### 要不然哩

%%%%%%%%%%%%%%%
!SLIDE x=0 y=4200 z=-3000 scale=2 slogen

## 為了將之開源，我們要把它包裝好

%%%%%%%%%%%%%%%
!SLIDE x=0 y=4200 z=-6000 scale=2 slogen many_subtitle

## 為何？

#### 方便推坑

#### 撿到新機器的時候，可以瞬間將之馴服

#### 然後就可以自動化了

%%%%%%%%%%%%%%%
!SLIDE x=0 y=4200 z=-9000 scale=2 slogen

## 如何做？

#### 盡量使用別人寫好的框架

#### 寫好安裝包

%%%%%%%%%%%%%%%
!SLIDE x=0 y=6300 z=-9000 rotate-x=180 scale=3 slogen

## 雖然只是一些無聊的小東西

#### 但對我也不是毫無幫助

%%%%%%%%%%%%%%%
!SLIDE x=0 y=6300 z=-6000 rotate-x=180 scale=3 slogen

## 好處 #1

#### 我為了能夠包裝這些東西，學到了不少 unix 指令

%%%%%%%%%%%%%%%
!SLIDE x=0 y=6300 z=-3000 rotate-x=180 scale=3 slogen

## 好處 #2

#### 作為凡人的我們，可以從自己的小東西開始"練習"開源貢獻

#### 其實不見得一定是客製化，像是遊戲或是小工具也不錯啊

%%%%%%%%%%%%%%%
!SLIDE x=0 y=6300 z=0 rotate-x=180 scale=3 slogen

## 好處 #3

#### **可以跟別人炫耀**，可以讓別人了解你

%%%%%%%%%%%%%%%
!SLIDE x=0 y=6300 z=3000 rotate-x=180 scale=3 slogen

## 好處 #4

#### 這些是可以用的東西啊，自己用起來就是爽

%%%%%%%%%%%%%%%
!SLIDE x=-2000 y=4000 z=6000 rotate=90 scale=5 slogen

## 就這樣

#### 以上就是今天來跟大家分享的東西

%%%%%%%%%%%%%%%
!SLIDE x=-5000 y=4000 z=6000 rotate=90 scale=5 slogen many_subtitle picture

### 宣傳一下

#### [五倍紅寶石](http://5xruby.tw)，現正招募實習生！

#### [中興資訊社](http://nchuit.cc)，中區同學們，快來參與關注我們！

![5xruby_nchuit](http://i.imgur.com/na7TC81.png)

%%%%%%%%%%%%%%%
!SLIDE x=-8000 y=4000 z=6000 rotate=90 scale=5 center-list

### 最後，一些東西

 * 本投影片位置：[http://ppt.cc/MXOs3](http://ppt.cc/MXOs3) 以及 [Repo](https://github.com/chgu82837/SITCON_2016_myStyle)
 * 聯絡我：
    * 我的個人網站：[http://pastleo.me](http://pastleo.me)
    * [http://fb.me/pastleo](http://fb.me/pastleo)

#### 請鞭小力點

#### 謝謝大家

%% The End
%%%%%%%%%%%%%%%
