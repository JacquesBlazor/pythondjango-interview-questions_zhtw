# pythondjango-interview-questions_zhtw
This is a traslation from django-interview-questions (https://github.com/the5fire/django-interview-questions)

# Django Web開發技術棧 - 面試常見問題整理

這篇內容是摘自[《Django企業開發實戰》](https://www.the5fire.com/983.html)，這是這本書在讓[大媽（Zoom.Quiet)](https://github.com/ZoomQuiet) Review 時，大媽給的建議。

出版物的生命周期比較短，索性放開到Github上，集眾人智慧，構建一個能供所有想要學習 Python Web 開發或者 Django 的一個參考，與其說是面試參考，不如說是知識點清單，供大家查漏補缺，進一步提高自己的「戰鬥能力」。

目前只是可能會問到的問題或者知識點，還沒有對應的答案，答案歡迎大家透過 issues 的方式來參與。

倉庫地址: https://github.com/the5fire/django-interview-questions ，歡迎 star，歡迎貢獻內容。

## 1. Python基礎

* 基礎語法是否熟悉？介紹下。
* 有哪些關鍵字，並且解釋其作用？
* 有哪些內置方法，並且解釋其作用？
* 解釋下什麼是動態語言？動態強類型是指什麼？
* 是否有編碼規範的概念？採用的是哪中編碼規範？
* 解釋下深拷貝和淺拷貝
* lambda的用法以及使用場景？
* 解釋下什麼是閉包，以及它的作用？
* 實現一個簡單的裝飾器，用來對某個函數的結果進行緩存？
* Python中幾種容器類型的差別及使用場景？
* 列表推導式的使用和場景？
* yield的使用。
* 常用的內置庫有哪些？舉例他們的用法。
* 介紹下你了解的"dunder method"（魔法方法）有哪些，以及他們的作用？
* 解釋下面向物件的概念，以及在編程中的作用？
* 如何實現單例模式？
* 如何對Python物件進行序列化？
* 是否能夠熟練編寫多線程和多進程程式？
* 使用socket編寫一個簡單的HTTP Server，成功回傳success即可。
* 如何理解Python中的GIL？對我們日常開發有什麼影響？
* 解釋下協程、線程、進程之間的差別。


## 2. Django基礎

#### 整體結構

* 如何理解設計模式中的MVC模式，你日常中怎麼使用這種模式？
* 如何理解Django中的MTV模型？
* 介紹下Django中你熟悉的模組有哪些，分別作用是什麼？
* 如何看待Django內建的Admin，以及說說你的使用經驗。
* 如何理解WSGI的作用？
* 如何自己實現WSGI協議？
* 為什麼正式部署時不要開啟``DEBUG = True``設定？

#### Model層

* 如何理解Django Migrations的作用？
* 是否有過手動編輯Migrations文件的經歷，原因是什麼，有哪些需要注意的？
* 介紹下ORM的概念。
* 如何理解ORM在Django框架中的作用？
* 介紹下ORM下的N+1問題，發生的原因，以及解決方案。
* 介紹下Django中Model的作用。
* Model的Meta屬性類有哪些可設定項，作用是什麼，日常用到的。
* 介紹下QuerySet的作用，以及你常用的QuerySet優化措施？
* 介紹下Pagination的使用。
* 介紹下Model中Field的作用。
* 如何定制Manager？什麼場景下需要定制？
* Raw SQL的效率跟ORM的效率是否進行過對比，結果如何？如何理解這種差異？
* Django內置提供的權限邏輯是什麼，以及其粒度？

#### View層

* Django中function view和Class-based View的差別及適用場景？
* 如何給Class-based View增加login required裝飾器？
* Middleware在Django系統中的作用？
* settings中預設設定的MIDDLEWARES有哪些？他們的作用分別是什麼？是否可以移除？
* Django系統如何判斷用戶是否為登錄用戶？
* 對於無Cookie的瀏覽器如何實現用戶登錄？
* Django中的request和HttpResponse的作用是什麼？
* 如何處理圖片上傳的邏輯，以及顯示邏輯？
* 介紹下用到過的Django的緩存粒度。

#### Form層

* 介紹下Django中Form的作用。
* Form中的Field跟Model中的Field有何關聯？
* 如何在Form層實現對某個欄位的校驗？

#### Template層

* 如何理解Django範本對設計師友好的說法？
* 日常開發中如何規劃Django的範本繼承和include？
* 常用的標籤（tag）和過濾器（filter）有哪些？
* 在範本中如何處理靜態文件？
* 在範本中如何處理系統內定義的URL？
* 如何自定義標籤和過濾器？


## 3. Django進階

* 如何排查Django專案的性能問題？
* 如何部署Django專案，以及不同的部署方式之間的差別？
* 部署時如何處理專案中的靜態文件？
* 如何實現自定義的登錄認證邏輯？
* 如何理解Django中Model、Form、ModelForm和Field、Widgets之間的關聯？
* Paginator的原理是什麼，如何自己實現分頁邏輯?
* Model中Field的作用是什麼？
* 什麼是SQL注入，ORM又是如何解決這個問題的？
* CSRF全稱是什麼？Django是如何解決這個問題的？
* XSS攻擊是指什麼，在開發時應該如何避免這種攻擊？
* Signal的作用以及實現邏輯？
* DATABASE設定中的``CONN_MAX_AGE``參數的作用，以及使用場景？
* ``CONN_MAX_AGE``的實現邏輯是什麼？
* 用Django內置的User模型建立用戶時是否可以直接:``User(username='the5fire', password='the5fire').save()``？
* 上面的建立方式有什麼問題？應該如何處理用戶密碼？
* 使用Django-rest-framework如何實現用戶認證登錄邏輯？
* Session模組在Django中的作用是什麼？
* 如何自定義Django中的權限粒度，實現自己的權限邏輯？
* 如何擷取線上系統的異常？
* 如何分析某個接口回應時間過長的問題，假設回應時間為2秒，一次請求涉及到資料庫和緩存查詢。


## 4. 部署相關

* 如何來自動化部署專案到生產環境，具體流程？
* 介紹下常用的自動化部署工具？
* 用到哪些監控工具，作用是什麼，使用中有什麼不足之處？
* Supervisor的作用是什麼？為何使用它？
* Gunicorn的作用是什麼？為何使用它？
* 如何對系統進行壓測？以及流量預估？
* Nginx的作用是什麼？是否能獨立設定？有沒有優化經驗？
* 發版邏輯是什麼，如何保證新版本發生異常時能快速回滾？


## 5. MySQL資料庫

* 如何確定需要哪些欄位需要設定索引？
* 什麼情況下需要設定欄位屬性為``unique = True``？
* 如何排查某個SQL語句的索引命中情況？
* 如何排查查詢過慢的SQL語句？

## 6. Redis

* 你了解的Redis的特點是什麼？為什麼會使用它？
* 支援的資料類型
* 如何合理的規劃key？
* 例如我需要把所有的文章和分類資料寫入Redis，在Django中直接讀取Redis拿到分類和文章的資料，問怎麼規劃資料存儲，如何處理分頁？
* 是否支援交易？舉個例子。
* 有哪些資料淘汰策略？
* 當你發現有些Redis查詢回應時間太長，如何排查？可能是什麼引起的？
* 你用到的或者了解的Redis的部署結構是什麼？
* 是否了解Redis的持久化策略，不同的策略有什麼不同？
* 說說你了解的Redis主從同步的策略。


## 7. 常用算法

* Python中字典類型的實現算法？
* 你了解的高級語言中的垃圾回收機制有哪些？Python中用的是什麼？
* 介紹下你知道的緩存相關的算法？
* 介紹下你知道的負載均衡相關的算法？
* 介紹下資料庫索引相關算法？


## 8. 總結

上面列的很多內容都已經超出了Django的範圍，但依然是屬於Web開發領域需要掌握的知識。

就Django本身來說，它只是Python眾多Web開發框架中的一個，單純的掌握Django的使用並不能讓你滿足企業中對Web開發的需求。因此把本書作為你開啟Web開發之路的起點，在扎實地掌握Django使用之後，可以由此展開，去涉及Web開發的方方面面。


*廣告*

京東：[《Django企業開發實戰 高效Python Web框架指南》(胡陽)【摘要 書評 試讀】- 京東圖書](https://item.jd.com/12537842.html)

當當：[Django企業開發實戰 高效Python Web框架指南](http://product.dangdang.com/26509799.html)
