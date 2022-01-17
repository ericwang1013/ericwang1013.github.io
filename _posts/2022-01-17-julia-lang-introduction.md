---
layout: post #Do not change.
category: [dataanalysis, julia] #One, more categories or no at all.
title:  "Julia 學習筆記-000"
date:   2022-01-17
author: Eric #Author's nick.
---

# 前言 #
目前手邊資料將它稱之為  
**「新世代資料科學與數值運算語言」**  
學習資料：[Julia 程式設計 第二版](https://www.books.com.tw/products/0010824245 "Title")

<a href="/assets/img/posts/julialogo.jpg" data-lity class="sx-center">
  <img src="/assets/img/posts/julialogo_thumb.jpg"/>
</a>

圖片來源：https://news.mit.edu/2018/mit-developed-julia-programming-language-debuts-juliacon-0827

# 介紹 #
Julia 是個新興的程式語言，在2009年開始這個專案，並在2012年發表。  
最大特色就是它同時兼具 **高效能** 和 **高階語法** 。  

_「Whrit like Python, run like C.」_  

Julia 是一個**泛用型語言(General Purpose Language)**。  
它支援 **多典範(Mulit-Paradigm)** 的程式設計風格、基於 **多重分派(Multi Dispatch)** 的(類)物件導向程式設計、程序式(Procedural)程式設計、函數式(Functional)程式設計與 **Metaprogramming** 。  
並且它內建 **套件管理器** 。  
因為與法的設計可以使用執行緒及行程進行 **平行運算** ，並且內建叢集管理器，可以達成 **分散式運算** 。  

# 理念 #
- 更高速的運算速度：所以使用了 **LLVM編譯器框架** 可進行 **即時編譯(JIT)** 。
- 採用更直接的語法
- 動態型別：可以指定變數的型別，也可以創建具有 **層次結構** 的型別來處理特定型別變數。如果在特定的情境不需要型別，也可以完全不輸入型別。
- 可以載入 Python 和 C 的套件(Package)：也可以透過 PyCall 套件與 Python Code 進行互動。此外，和 Python 之間的資料可以共享。
- Metaprogramming：Julia 程式可以生成其他 Julia 程式，甚至可以修改自己的程式碼。

# 比較 #
目前資料科學的主流語言是 Python，所以兩者之間有甚麼不同之處。  

## Julia 與 Python 兩者差異 ##
1. Julia 的索引值是從「**1**」開始，而不是從 0 開始。
2. 索引列表和數組的最後一個元素， Julia 使用 **結束(end)** ， Python 則使用 **-1** 。
3. Julia 在 for, if, while 等區塊的結尾需要end，但不強制要求縮排。
4. Julia 沒有分行語法支援；如果在一行的結尾，輸入已經是個完整的表達式，就會直接執行，或是繼續等待輸入。

## Julia 的優勢 ##
1. 速度更快
2. 友善的數學語法
3. 自動記憶體管理
4. 平行性

## Python 的優勢 ##
1. 索引值從「**0**」開始
2. 豐富的第三方套件
3. 具有龐大的開發社群支援
4. 學習資源

# 總結 #
各種程式語言都會有其所可發揮之處，端看使用者怎麼發揮囉。
