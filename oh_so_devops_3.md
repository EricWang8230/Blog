# DevOps Moment / Oh. So. DevOps
* 本文章只代表我個人自身經驗如有傳達的觀念或知識錯誤的還請提出，謝謝。

每次做維護時(不管是雲端或是地端)都會有人好奇想要了解:
* 在維護什麼?
* 為什麼需要維護? 
* 為什麼時間這麼長?
* 為什麼維護時間不是正常上班時間?
* etc...

今天就來分享維護窗口在幹嘛以及我在規劃一個維護窗口的思路和一些`有趣`的維護經驗，同時也歡迎大家分享自身的維護窗口經驗。

<br>

# 什麼是維護窗口(Maintenance window)?
開始前可以閱讀這篇[Wiki](https://en.wikipedia.org/wiki/Maintenance_window)了解什麼是維護窗口，以下是從Wiki擷取的一段話:

```
維護窗口是維運人員預先指定的一段時間，在此期間可以進行可能導致服務中斷的預防性維護。
```

我個人覺得[歲修](https://pedia.cloud.edu.tw/Entry/Detail/?title=%E6%AD%B2%E4%BF%AE)也算是一總維護窗口。

<br>

# 分享我是如何規劃維護窗口
廢話不多說直接來看我準備一個維護窗口時會考慮哪些事情，我分為三大部分:

* 事前準備:
  * 安排停機日期及時間
  * 維護`前` N 週/天發出公告通知/提醒客戶
  * 確認備份機制正常運行
  * 確認還原機制可以運行
  * 通知原廠技術支援待命
  * 釐清維護的範圍
  * 釐清維護所需的工程師人數
  * 釐清每個人負責的範圍
  * 閱讀Release Note
  * 列出維護後如何驗證問題修復
  * 列出維護時可能會遇到的問題(最壞打算)
  * 準備可能會遇到的問題的解決方案
  * 撰寫自動化腳本(驗證, 維護, etc...)
  * 在測試環境中測試流程及腳本
  * 反覆模擬/練習十次

<br>

* 開始維護:
  * 不在預料內的突發狀況
  * 了解進度並判斷情勢

<br>

* 結束維護:
  * 復原
  * 驗證
  * 上線
  * 公告維護結束
  * 觀察維護後有無不預期的行為
  * 恭喜下班

以上的準備清單是以我自己6年的維運經驗以及40-50次大大小小的維護經驗，小時候不懂事熱血就衝了踩了不少地雷跌跌撞撞摸索出來的清單，也歡迎大家分享自己在維護時都是怎麼做準備的。

接下來我會依照上面的大項目開始一一細談每個環節的重點是什麼。
