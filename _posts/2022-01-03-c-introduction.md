---
layout: post #Do not change.
category: [programming, c] #One, more categories or no at all.
title:  "C 學習筆記-000"
date:   2022-01-03
author: Eric #Author's nick.
---

# 前言 #
在最近的面試中，發現了**C**才是最主要的工作語言。  
因此應該是要先把以前所學的重新複習一遍才對。  
學習資料：[C語言教學手冊](https://www.books.com.tw/products/0010360466 "Title")

<a href="/assets/img/posts/clogo.jpg" data-lity class="sx-center">
  <img src="/assets/img/posts/clogo_thumb.jpg"/>
</a>

圖片來源：https://www.jalalmhz.ir/web-design-and-development/introduction-to-c-programming-language/2021/05/19/

# 筆記 #
**高效率的編譯式語言**

**介於高階與低階之間的語言**
- 有低階語言的優點，執行效率高、硬體控制好。
- 有高階語言的優點，易於編寫、除錯。
- 並且容易與結合語言連結。

**靈活的程式控制流程**  
程式語言的可攜性(Portability)就如同硬體的相容性(Compatibility)。  
所謂的「可攜性佳」，意味著在某一作業系統上所編寫的程式碼，可以在少量修改或完全不修改的情況下即可在另一個作業系統上執行。

**為程式設計師所設計的語言**
- 可以直接依記憶體的位址來存取變數，以提高程式執行的效率。
- 有豐富的運算子(Operator)。
- 有良好的函數庫(Library)。

# 編寫 #
良好的編寫習慣養成，可以透過六個步驟達成。

(1) 規劃程式  
    繪製流程圖，將程式的起始到結束的過程列出。

(2) 編寫程式碼及註解  
    適時在程式中加上註解，可增加程式的可讀性，也減輕後續維護的困難。

(3) 編譯與連結程式  
(4) 執行程式  
(5) 除錯與測試  
- 語意錯誤(Semantic error)：語法沒錯，但邏輯有誤。
- 語法錯誤(Syntax error)。

(6) 程式碼的修飾與儲存  
    必要將原始程式碼儲存備份。  

編寫時，須注意**大小寫**！因為在C語言的語法中，大小寫是有分別的。  

# 編譯 #
在編譯的過程中會產生一個「目的檔」(Object file)。  

什麼是目的檔？  
當編譯器進行編譯時，編譯器除了要檢查原始程式碼的語法是否正確外，還要將標頭檔(Header file)讀進來，並根據這個標頭黨內所記載的函數原型(prototype)，檢查程式碼中所使用到的函數用法是否合乎規則。當所有檢查都沒有發現錯誤時，編譯器就會產生一個目的檔。因此目的檔可視為一個已經編譯過且沒有錯誤的程式。

# 執行 #
有目的檔後，即可連結程式(linker)。  
連結程式是指會將其他的目的檔及函數庫連結在一起，產生一個可執行的檔案(.exe)。  

什麼是函數庫？  
函數為C語言的基本單位。因此許多不同的常用函數集合而成，即是函數庫。  

