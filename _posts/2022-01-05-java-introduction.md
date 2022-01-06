---
layout: post #Do not change.
category: [programming, java] #One, more categories or no at all.
title:  "Java 複習筆記-000"
date:   2022-01-05
author: Eric #Author's nick.
---

# 前言 #
跟 C 一樣是複習之前所學的。  
學習資料：[Java語言教學手冊](https://www.books.com.tw/products/0010555220 "Title")

<a href="/assets/img/posts/javalogo.jpg" data-lity class="sx-center">
  <img src="/assets/img/posts/javalogo_thumb.jpg"/>
</a>

圖片來源：https://seekvectors.com/post/java-logo

# 筆記 #
Java的開發工具稱為 Java Development Kit，簡稱JDK。  
JDK可分為三個版本，分別為J2SE(Java 2 Standard Edition)、J2ME(Java 2 Micro Edition)、J2EE(Java 2 Enterprise Edition)。
- J2SE，定位於用戶端的程式設計。
- J2EE，伺服器端程式的應用設計。
- J2ME，用於嵌入式系統開發設計。

**嬌小且完美的語言**  

**具物件導向的功能**  

**完全支援網際網路**  

**通用的語言**  

**跨平台的語言**  

**具有豐富的函數庫**  

**特殊的處理機制**  

# 執行 #
Java的執行方式比較特殊。它必須先經過編譯的程序，然後再利用直譯的方式來執行。  
透過編譯器，Java程式碼會被轉成與平台無關的機器碼，稱之為「**位元組碼**」(bytecode)，然後再透過直譯器便可解譯並執行該位元組碼。  
而任何一種可以執行Java的軟體，都可以看成是Java的**虛擬機器**(JVM)，所以，位元組碼就是虛擬機器可以執行的機器碼。  
也就產生最大的好處：可跨越平台執行！  
**『撰寫一次，到處執行。』**  

# 差異 #
Java應用程式(**application**)：是指可以在Java平台上獨立執行的程式。  
Java網頁程式(**applet**)：是指內嵌於html檔裡，然後搭配瀏覽器來執行的程式。  
