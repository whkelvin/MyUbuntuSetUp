<a name="hello-world"></a>
# Hello World!
![](https://github.com/whkelvin/MyUbuntuSetUp/blob/master/Pictures/ubuntu.png)
![](https://github.com/whkelvin/MyUbuntuSetUp/blob/master/Pictures/ubuntu.gif)

<a name="intro"></a>
# 簡介
各位看到上面兩張圖就手癢的同學你們好！我絕對不會和你們說我在Dcard上發文發現有了一個小粉絲後, 就迫不及待加興高采烈的跑來寫一篇新手+懶人向教學文, 順便介紹一下我的set up。那就廢話不多說先上TOC囉。

- [Hello World!](#hello-world)
- [簡介](#intro)
- [規格 Requirement](#requirement)
  * [作業系統 Operating System](#operating-system)
- [主題 Theme](#theme)
  * [Nord Theme](#nord-theme)
- [桌面背景 Wallpaper](#wallpaper)
- [桌面環境/視窗管理員 Desktop Environment/Window Manager](#desktop-environment-window-manager)
  * [Gnome Theme](#gnome)
      * [Application Theme](#application-theme)
  * [i3](#i3)
  * [polybar](#polybar)
- [虛擬終端 Terminal Emulator](#terminal-emulator)
  * [Alacritty](#alacritty)
  * [Fish Shell](#fish-shell)
  * [Powerline](#powerline)
  * [neofetch](#neofetch)
  * [cmatrix & unimatrix](#cmatrix-unimatrix)
  * [cava](#cava)

- [License](#license)


<a name="requirement"></a>
# 規格 Requirement

<a name="operating-system"></a>
## 作業系統 Operating System
[Ubuntu 20.04.1 LTS](https://ubuntu.com/download/desktop) (舊一點的應該也沒問題, 只要是Linux基本上都可以[Android 別鬧], 這篇會以ubuntu為主, 其他Distro請到樓下的官網自己爬文謝謝)

Mac & Windows - ~~丟掉你的電腦, 我是說微軟或Apple拜託請我~~ 如果想試試Linux可以裝[Virtual Machine](https://www.virtualbox.org/) 或是 [Dual Boot](https://zh.wikipedia.org/wiki/%E5%A4%9A%E9%87%8D%E5%BC%95%E5%AF%BC)或是~~資助我一台Macbook~~

Mac & WSL - 有一些Terminal Emulator裡的程式是有支援的, 請到樓下的官網自己爬文謝謝
<a name="theme"></a>
# 主題 Theme

<a name="nord-theme"></a>
## Nord Theme
[官網](https://www.nordtheme.com/ports)
[Github Repo](https://github.com/arcticicestudio/nord)

這麼美的主題我還不用爆。[官方支援](https://www.nordtheme.com/ports)的程式超多, 官網上列的有些還沒有內容其實都在github repo,可以去找找。我的配色很多也是參考（ㄔㄠ ㄒㄧˊ）他們的調色盤。非官方的主題也不少, 像是瀏覽器的[主題](https://chrome.google.com/webstore/detail/nord/abehfkkfjlplnjadfcjiflnejblfmmpj/reviews)等等。順帶一提, 還在用Google Chrome, Edge 和 IE(???)的大大們, 該換[瀏覽器](https://brave.com/)囉。以後寫一篇文專門為大家講解Brave Browser(喂。

<a name="wallpaper"></a>
# 桌面背景 Wallpaper
我自己用[Inkscape](https://inkscape.org/)畫的, 麻煩到[這裡](https://github.com/whkelvin/MyUbuntuSetUp/issues)稱讚我。(~~就你issues最多~~)

PNG 和 SVG檔都在[這裡](https://github.com/whkelvin/MyUbuntuSetUp/tree/master/Pictures), 如果賣出去拜託讓我抽個成我的學貸還不完QAQ

<a name="desktop-environment-window-manager"></a>
# 桌面環境/視窗管理員 Desktop Environment(DE)/Window Manager(WM)
熱騰騰剛裝好的Ubuntu20.04桌面長這樣。

![](https://github.com/whkelvin/MyUbuntuSetUp/blob/master/Pictures/default_desktop.png)

~~這不是肯德基~~ 剛裝好的時候覺得預設的桌面蠻酷的，不過五分鐘後我就把能換的東西都換了.... Linux和Mac OS & Windows最大的不同的地方就在於看到不喜歡的東西全部通通都可以改,不想看到的東西也可以藏起來。你想要的話也能今天讓你的桌面還有視窗看起來像[Mac OS](https://itsfoss.com/make-ubuntu-look-like-macos/),明天看起來像[Windows](https://www.makeuseof.com/tag/make-linux-look-like-windows/)，不過何必為難自己呢？ 既然都在看這篇了不如自己做出一個屬於你自己的獨一無二的桌面，讓上課坐你隔壁的同學下巴都掉下來嘿嘿。

桌面環境是什麼呢？簡單的說他就是你開機之後會看到的UI。Ubuntu20.04預設的桌面環境是[Gnome](https://www.gnome.org/), 上圖螢幕左邊的Apps還有上面的狀態列（中間有時間,旁邊還有一些音量按鈕的那個）都是Gnome DE(Desktop Environment)的一部分。還有像是視窗右上角的放大縮小按鈕樣式也都是由Gnome DE提供的，更準確的說視窗裡的按鈕是由Gnome DE裡面的視窗管理員(Window Manager)掌管的。視窗管裡員的工作就是幫你排版你的視窗，調整視窗大小還有顯示跟視窗相關的按鈕等等。

為什麼要提到這麼這麼多細節呢？在Mac/Windows的世界裡你可能永遠也不需要知道視窗管理員是什麼。那是因為在Linux世界裡，很多的大神都不用DE, 沒錯，在登入的時候你可以選擇要使用桌面環境或是只要用純粹的視窗管理員。有些視窗管理員會提供預設的簡單狀態列，不過大部分的都是走什麼都沒有的極簡風格，登入之後看到的就只有你的背景圖，滑鼠基本上是廢了，沒有東西給你按。這樣的好處呢就是你愛加什麼就加什麼，全部都由你決定。當然，不建議新手這樣搞，以後寫一篇文專門跟大家解釋到底~~哪個吃飽太閒的瘋子會這樣弄~~。

<a name="gnome"></a>
## Gnome Theme

<a name="application-theme"></a>
### Application Theme
這是預設的主題:
![](https://github.com/whkelvin/MyUbuntuSetUp/blob/master/Pictures/default_app.png)
這是改完之後的樣子:
![](https://github.com/whkelvin/MyUbuntuSetUp/blob/master/Pictures/nordic_app.png)

首先我們要安裝gnome-tweaks:
gnome-tweaks是一個提供預設的設定裡沒有的選項的設定程式，我們會用他來更換主題。

將universe repo加到apt裡：
``` sudo add-apt-repository universe ```

更新apt裡的package:
``` sudo apt update ```

更新系統裡的軟體:
``` sudo apt upgrade ```

安裝gnome-tweaks
``` sudo apt install gnome-tweaks ```

- apt 是Ubuntu的package manager, 有點類似Google Play 或 App Store
- sudo 是一個讓你在terminal暫時提高權限的指令。

![](https://github.com/whkelvin/MyUbuntuSetUp/blob/master/Pictures/tweaks.png)
打開tweaks之後可以到Appearance->Themes->Application選擇你喜歡的主題。

如果想要nord的顏色的話, 可以到[這裡](https://www.gnome-look.org/p/1267246/)下載（我選nordic-darker, 你可以選你喜歡的）。下載下來的檔案解壓縮之後放到`~/.themes` 裡。

**注意**
- `.themes`這個資料夾不存在的話你會需要建一個新的資料夾,而所有檔名是`.`開始的都會被藏起來。在Files裡記得顯示隱藏的檔案。

![](https://github.com/whkelvin/MyUbuntuSetUp/blob/master/Pictures/show_hidden.png)
我的`~/.themes`長這樣。
![](https://github.com/whkelvin/MyUbuntuSetUp/blob/master/Pictures/theme_folder.png)
然後從重新打開tweaks->Appearance->Themes->Application就應該可以看到新的主題啦。
![](https://github.com/whkelvin/MyUbuntuSietUp/blob/master/Pictures/tweak_nordic.png)

### Icon Theme
![](https://github.com/whkelvin/MyUbuntuSetUp/blob/master/Pictures/flat_icon.png)
沒有錯，連App的Icon都可以改。我用的Icon Theme是[這個](https://www.opendesktop.org/p/1012431)
我選的是05-Flat-Remix-Green-Dark,注意左側App的icons還有檔案的圖片都不一樣了。一樣把下載下來的檔案解壓縮放到`~/.icons`裡。之後就可以在tweaks->Appearance->Themes->Icons裡面看到啦！

**注意:**

- **`.icons`這個資料夾不存在的話你會需要建一個新的資料夾,而所有檔名是`.`開始的都會被藏起來。在Files裡記得顯示隱藏的檔案。**

- **我解壓縮完的時候發現要把解出來的檔案夾裡的檔案夾貼到`~/.icons`才行。**

### Dash to Dock
最後再來分享個小撇步，可以讓你把原本在左邊的App Bar移到下面，然後縮小一點。
![](https://github.com/whkelvin/MyUbuntuSetUp/blob/master/Pictures/dash_to_dock.png)

<a name="i3"></a>
## i3
coming soon...

<a name="polybar"></a>
### polybar
coming soon...

<a name="terminal-emulator"></a>
# 虛擬終端 Terminal Emulator
剛開始用Linux的時候完全搞不清楚什麼是Terminal Emulator什麼是Shell,反正一開始都用預設的,也不覺得有什麼問題。後來慢慢熟了之後才開始踏出舒適圈,去查各種專有名詞,試試預設外的別種口味,然後變得越來越挑食... 總之覺得在跳進Terminal的世界裡之前好像要解釋一下Terminal Emulator & Shell 有什麼不同。

Terminal（Terminal Emulator）是一個你可以對你的電腦上下其手的地方>///<。在Terminal裡面你可以下各種指令來和你的電腦互動,像是列出電腦裡有什麼檔案之類的。Terminal 提供的只是一個介面，讀取你鍵盤的輸入，還有顯示每個指令的結果。

每個Terminal裡面都住了一個Shell,這個Shell就是實際去執行你的指令的傢伙。

Ubuntu 20.04預設的Terminal是Gnome Terminal, 而預設的Shell是Bash。
Mac OS 裡也有Mac Terminal, 預設的Shell也是Bash,不過好像似乎最近有換。
Win 10 我是用Windows Terminal,預設的Shell應該是powershell。

Terminal和Shell的選擇千百種,可以自己去Google挑,當然要有小三也不是不行,畢竟小孩紙才做選擇嘿。參考我底下的推薦也可以，反正Linux推崇的就是共享(貴圈真亂

注意：很多在Terminal裡面跑的程式都會用到Terminal裡設置的顏色,所以建議要先把Terminal的主題換成Nord。

<a name="alacritty"></a>
## Alacritty
[Github Repo](https://github.com/alacritty/alacritty)

Alacritty是號稱全世界最快的Terminal。目前還在[Beta](https://zh.wikipedia.org/wiki/%E8%BB%9F%E4%BB%B6%E7%89%88%E6%9C%AC%E9%80%B1%E6%9C%9F)開發階段,不過我目前用起來好像沒碰到什麼Bug。

### 安裝
之前自己裝的時候我是直接[build from source](https://zh.wikipedia.org/wiki/%E8%BB%9F%E9%AB%94%E7%B5%84%E5%BB%BA),因為用官方上列的簡單方法一直出錯,不推薦新手這樣裝,免得還沒裝好血就吐完了。有勇者想試試可以來[這裡](https://github.com/alacritty/alacritty/blob/master/INSTALL.md#debianubuntu)。

你也可以試試
``` cargo install alacritty ```
說不定平常有扶老奶奶過馬路就成功了也不一定。

裝成功的話
``` alacritty ``` 就可以打開一個新的視窗囉。

### Nord 主題
Alacritty 的設置都放在``` ~/.config/alacritty/alacritty.yml``` 
來[這裡](https://github.com/arcticicestudio/nord-alacritty/blob/develop/src/nord.yml)複製nord的顏色放到alacritty.yml裡面,然後存檔重新開Alacritty應該就可以看到顏色不同啦。注意yml檔案裡的空格很重要,該有空格沒空格就會出錯,還有記得前面有#的都是注釋,可以順便把你想改的值也都改一改。

<a name="gnome-terminal"></a>
## Gnome Terminal
Nord 也是有支援Ubuntu的Gnome Terminal, 
<a name="fish-shell"></a>
## Fish Shell
coming soon...

<a name="powerline"></a>
## Powerline
coming soon...

<a name="neofetch"></a>
## neofetch
coming soon...

<a name="cmatrix-unimatrix"></a>
## cmatrix & unimatrix
coming soon...

<a name="cava"></a>
## cava
coming soon...

<a name="license"></a>
# License
[WTFPL – Do What the Fuck You Want to Public License](http://www.wtfpl.net/)
隨你怎麼改license, 不用謝。


