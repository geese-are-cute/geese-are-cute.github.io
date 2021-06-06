上課心得

幸好有上課錄影可以看，

老師上課經常回答同學問題，且常常離題，上課的步調進度其實是緩慢的

看影片時須利用快轉，提高觀看效率，抓重點

我不喜歡邊聽課邊做筆記，因為我很不擅長多工

筆記不錯的童鞋：古世強、趙雨萱、高子薇、詹雲翔、張雅屏、吳承恩、李資民、彭郁文

00-43-57 之前：上課前隨堂測試

00-43-57 -

#### XHR (XMLHttpRequest)

- 類似 fetch, jQuery ajax, axios
- 原生基礎，在 fetch, jQuery ajax ..... 出現前就存在，是他們的基礎

#### 展示同步和非同步的差異

00-48-28 demo 同步和非同步 index.html
00-50-20 aws 的講義
00-52-14 老師建立 server
01-01-55 server 建好，老師準備講解

打：送出請求

01-04-18 解釋 XMLHttpRequest

> 簡單來說就是發一個 Http 請求

https://developer.mozilla.org/zh-TW/docs/Web/API/XMLHttpRequest/Using_XMLHttpRequest

01-05-09 對老師的網站（server）發出請求

> fetch 我不知道，但是 jQuery 的底層就是用 XMLHttpRequest
> XMLHttpRequest 可以是同步也可以是非同步
> 同步的請求會有 Blocking 問題所以在網頁上使用較不友善，但還是有一定要使用同步請求的時機（老師舉的十年前例子：股票下單）
> 同步相對於非同步使用機會是很稀少的，但不是沒有

01-06-55 解釋 Code
01-09-07 XML vs Json vs HTML
01-13-40 建立 XML 物件
01-16-13 ？？？ response 是 xhr.onload 傳回來的東西嗎？
https://javascript.info/onload-onerror

https://developer.mozilla.org/zh-CN/docs/Web/API/XMLHttpRequestEventTarget/onload

01-17-10 需要檢查 status 200 嗎？
01-17-39 this.responseText

01-20-36 示範同步（之前是示範非同步）

有些事執行比較花時間，如 I/O、發出請求之類的。
JS 是但執行緒的語言，如果 JS 都用同步方式做以上的事，就很容易產生 blocking 情形。
所以可能較花時間的事，往往被設計成是非同步方式執行

瀏覽器警告 Synchronous XMLHttpRequest on the main thread is deprecated because of its detrimental effects to the end user's experience. For more help, check http: //xhr.spec.whatwg.org/.

> 這可能是你們這輩子唯一一次做 XMLHttpRequest 請求

01-26-10 ~ 01-31-26 同學練習
01-31-26 ~ 01-32-50 解釋 onload 和 send 的差異

01-39-41 ？？？螢幕截圖那邊 line 33 ~ 35 是在 send() 之前，好像不合邏輯，還是說因為他是 asynch? 等等，好像不是這樣，回想一下 onclick 的例子

- 我拿原始檔試了一下，send() 放在 onload 之前或之後都是沒差的

01-40-01 Ajax 教學投影片，重要（抄）
- XML 是 legacy technology（現在幾乎沒有再使用了）
- 01-41-43 devtool 的network界面，每一條綠線都是對伺服器發出請求
    - 發請求方式1：重新整理網頁（比較慢）
    -
- 01-43-08 onreadystatechange
- 01-44-42 onreadystatechange vs onload
- 01-45-45 xhr.onload = function(response){ ........}  那個 response 其實是錯的，所以拿掉
- 01-49-03 現在這個 代沒有人再用 XMLHttpRequest，都改用 fetch、ajax、axios
- 01-49-30 XMLHttpRequest 是底層（瀏覽器原生提供的）：
    - jQuery 只是把XMLHttpRequest包裝起來
    - 01-50-50 axios：axios 如何判斷使用瀏覽器/node.JS （XMLHttpRequest）,參考下圖
    ![](https://i.imgur.com/JcXqMC2.png)
    - XMLHttpRequest 是在以上圖片的那個部分？
- 01-53-41 研究 adapters/xhr，仔細看他底層還是使用 XMLHttpRequest 
- 段落

01-55-38 新主題 - 老師設定環境
01-57-25 CORS 同源政策，投影片抄一下（複習 protocol/domain/port）
02-01-13 不同源的時候，browser會幫你擋下來，但是其實browser 有送出請求，server也有收到請求 
02-02-49 為何要有同源政策：怕駭客
02-06-36 CORS是誰負責幫你擋？瀏覽器。除非伺服器告訴瀏覽器“我同意讓這些東西送”（預設是沒有同意的）
02-07-05 我們上次打證交所的資料是使用 node.js 沒有經過瀏覽器（node.js不擋）

自己去看 MDN CORS

02-11-13 換主題
02-16-37 老師示範上次的 crawler作業


下午
00-00-35 .gitignore、git rm --cached crawler/node_modules、有些檔案不需要上傳 github
00-01-52 
- package.json 的功能（npm 建立的）
- npm 套件管理系統、yarn
- package-lock.json: 鎖定目前的版本、自動產生、示範 00-03-36
- 00 04 54 - npm 有自己的 package.json 但套件也有自己的 package.json


00 07 39

01 47 14

02 02 47 callback 寫成同步的解答 











