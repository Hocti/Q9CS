# 九万輸入法

用九方 **已過期** 的專利 HK1035043 製作的中文輸入法
以numpad輸入2~3鍵即可開始選字

## 特色

- 免費
- 無需安裝、直接執行
- 支援emoji、香港增補字符集
- 用專用鍵進入"關聯字"表，不會影響首頁中 0 和 . 鍵功能
- 10個快速選字表，包括emoji，粵語字等 (可自行修改)
- 可自行以sqlite修改字碼、關聯字等
- numpad以外(如notebook)所有按鍵都可自行修改
- 可輸出簡體
- 可以拉到非常巨大 (正)

## 事先準備

.NET framework 4.8 或以上

如windows本身有安裝noto sans會優先使用，否則用回系統字體

由於可能存在法律爭議，碼表暫不公開，所以需要自己輸入字碼等資料\
玩家需自動修改files/img資料夾內的圖片\
以及files/dataset.db內，table "mapped_table"中的id 10  ~999 的字碼表\

推薦使用 SQLite Database Browser 修改\
https://sqlitebrowser.org/dl/

**當然如果有朋友已修改完後，直接把成果給你就最好啦**

## 下載

到[Releases](https://github.com/Hocti/Q9CS/releases/latest) 下載。

## 使用方法

|Key|功能|
| ---- | ---- |
|0~9.|和九方一樣|
|+|進入"關聯字"表<br />打下一個字之前，隨時可以按 + 進入選關聯字|
|-|a) (選字時) 上一頁<br />b) (首頁中) 快速選字表 (碼表1000)<br />c) (首頁按1~9後) 1~9號快速選字表 (碼表1001~1009)|
|*|開/關打同音字 (打完一個字後再揀字)，可以任何時間隨時開/關|
|/|開關引號，一次過輸 開+關 後兩個碼，如「」|
|F8|快速改變視窗大小|
|F9|快速改變視窗位置|
|F10|暫停/重啟輸入法|

## 快速選字表

在首頁按「numpad -」會進入快速選字表 0\
在首頁先按「1~9」再按「numpad -」會進入快速選字表 1~9\
可以自動修改files/dataset.db內，table "mapped_table"中的id 1000 ~1009 的 characters，改變這10個快速選字表內容

## 修改按鍵

除0-9.外，所有鍵都可以自行修改 tq9_settings.ini 內的keycode改變\
如不想用到的鍵，正以將keycode設定成0\
上一頁(prev)和快速選字(shortcut)鍵可以重複，預設兩個鍵都係 numpad * 鍵\
\
可以在這裡查到keycode:\
https://www.toptal.com/developers/keycode

## 不使用numpad

預設的0~9.是
|||
| ---- | ---- |
|qzxcr|[引號]789[同音]|
|asdfg|[上頁]456[關聯]|
|zxcvb| 0 123 .|

以上鍵都可以自行修改\
但在不使用numpad模式下，a-z鍵都不會正常運作\
想打a-z可以先按 f10 暫停輸入法

## Tray

在window start bar 右下角(tray menu)會找到 "九万" 的icon\
右鍵點選可選擇 關閉/輸入簡單/切換numpad輸入等