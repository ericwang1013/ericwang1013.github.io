---
layout: post #Do not change.
category: [dataanalysis, r] #One, more categories or no at all.
title:  "R 學習筆記-000"
date:   2022-01-17
author: Eric #Author's nick.
---

# 前言 #
老實說，R 在台灣其實不算大眾的程式語言。但我個人是看過它在 **統計** 上的應用後，覺得還是應該要學習它。  
學習資料：[輕鬆學習 R 語言 第二版](https://www.books.com.tw/products/0010835361 "Title")

<a href="/assets/img/posts/rlogo.jpg" data-lity class="sx-center">
  <img src="/assets/img/posts/rlogo_thumb.jpg"/>
</a>

# 介紹 #
R 語言是一個開源的統計程式語言，常用於開發統計和資料分析軟體系統。

# 特性 #
R 語言是以 **函數型(Functional)** 編程與 **資料分析** 為設計核心。  
因此，所有的資料(文字、數值或邏輯等)都 **不是以純量(Scalar)存在** ，而是 **以向量(Vector)存在** 。  
所以，R 語言是 **元素級別運算(Element-wise Operation)** 。

# 開發環境 #
直譯器，可從 R 官方網站下載。  
[The R Project for Statistical Computing](https://www.r-project.org/ "Title")  

整合式開發環境(IDE)，雖然也有其他開發器可用，但原生的還是比較好用。  
[R Studio](https://www.rstudio.com/ "Title")  

# 初始學習 #
賦值符號「**＜–**」；它的作用是將其右邊的值指派給符號左邊的物件。等同於其他程式語言中常用的「**＝**」運算子。事實上，「＝」也是可以在 R 語言上運用。  
(在 RStudio 上的快捷按法：alt + - )  

R 語言為物件命名的原則；  
1. 使用全小寫英文，不同單字之間以底線「ˍ」相隔。
2. 使用英文 **名詞** 為值(Values)和資料(Data)命名，使用英文 **動詞** 為函數(Functions)命名，這樣能讓名稱簡潔且具有意義。
3. 避免使用 **保留字** 與 **內建函數** 作為物件的命名。

R 語言的註解使用「**＃**」。  

# 內建函數 #
呼叫`print()`函數或物件名稱可以將物件內容輸出在Console(通常是指螢幕畫面上)。  
呼叫`rm()`函數將完成賦值的物件自環境中刪除，rm 是 remove 的縮寫。  
呼叫`help()`函數查詢資料以及函數的說明文件。  
呼叫`sessionInfo()`顯示 R 語言的版本與相關資訊。  
呼叫`Sys.getlocale()`顯示 R 語言的地區以及語言資訊。  
呼叫`getwd()`顯示 R 語言的工作目錄，wd 為 working directory 的縮寫。  
呼叫`setwd()`設定 R 語言的工作目錄，此處使用 Windows 作業系統的開發者要特別注意 **路徑斜線** 要使用 「**／**」正斜線，而不是系統所使用的反斜線「＼」。並且要避免在路徑設定上出現 **空格** 與 **非英文的文字** 。  

# 故障排除 #
R 語言的 Console 在預期使用者未完成輸入的時候會持續出現 ＋ 提示尚有指令需要輸入，常見的情景像是應該成對出現的雙引號、小括號、中括號與大括號，但卻並沒有輸入完成。  
所以排除方式有二；  
1. 在＋之後完成遺漏的輸入；
2. 在 Console 按 Esc 鍵離開，重新來過。

# 小結 #
新程式語言真的越來越簡潔了。
