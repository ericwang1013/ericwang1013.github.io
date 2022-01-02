---
layout: post #Do not change.
category: [ros] #One, more categories or no at all.
title:  "什麼是「ROS」？"
date:   2022-01-02
author: Eric #Author's nick.
---

# 前言 #
未來的產業趨勢，「機器人」顯然已經是要角之一！剛好藉著前工作(AMR)的機會，我也算是正式踏入了這個領域。
但，接下來想要擴展領域內的知識與應用，就要靠自己學習囉！

<a href="/assets/img/posts/roslogo.jpg" data-lity class="sx-center">
  <img src="/assets/img/posts/roslogo_thumb.jpg"/>
</a>

圖片來源：https://www.open-electronics.org/

# 什麼是ROS？ #

ROS是一種用於機器人的開源、基礎操作系統。它提供了您希望能從操作系統獲得的應用，包括了硬體抽象化、低階設備控制、常用功能的實現、運作之間的訊息傳遞和套件管理。它還提供用於在多台電腦上獲取、構建、編寫和運行程式碼的工具和函示庫。ROS在某些方面來解釋就形同於“機器人框架”，就如同以下所列的平台：Player、YARP、Orocos、CARMEN、Orca、MOOS和Microsoft Robotics Studio。

# 目標 #

當然也會有人問，“ROS與X究竟有什麼不同？”其中X是指其他機器人軟體平台。其實這是一個很難回答的問題，因為ROS的目標不是成為具有最多功能的框架。相反，ROS的主要目標是支援機器人研究和開發中的程式碼再利用。ROS是一個分佈式進程框架（又名：節點），它使可執行檔案能夠在運行時單獨設計和鬆散耦合。而這些運作方式又可以分別組合到套件和語法堆疊中，因此可以很容易地共享和分發。ROS還支援程式碼儲存庫的聯合系統，該系統也支持分佈式協作。從檔案系統級別到社群級別，還有支援關於開發和實施的獨立決策，會有這樣的設計，是將一切都能夠使用ROS基礎結構工具直接結合在一起。

為了支援共享和協作的主要目標，ROS框架還有其他幾個目標：

- 精簡：
ROS在初始設計時，就以精簡為目標。因為ROS並不是想要將開發者所編寫的main()函式等轉變成可執行檔或套件，而是要把在ROS底下所編寫出的程式碼能與其他機器人軟體平台做結合使用。 所以，ROS目前已經能夠與OpenRAVE、Orocos和Player等其他平台做相關結合應用。

- 半成品函式庫：
ROS的半成品函式庫，擁有簡潔的功能介面，而且容易編寫修改，很適合作為開發時的基礎首選。

- 語言獨立性：
ROS的運作框架也很容易透過任何現代程式語言進行實現。開發者已經在Python、C++和Lisp上持續發展，而後續也有了Java和Lua的實驗性函式庫可供研究。

- 易於測試：
ROS有一個名為 **rostest** 的內建單元/整合測試框架，可以輕鬆地在受測設備上運行與分別測試。

- 擴展性：
ROS適用於大型運作系統和大型開發流程。

# 運作環境 #

ROS目前僅能在Unix系統基礎的平台上運作，並且相關應用軟體主要都在Ubuntu和Mac OS X系統上進行測試，不過ROS社群也持續地替Fedora、Gentoo、Arch Linux等其他Linux平台提供相關技術支援。

雖然可以將ROS移植到Microsoft Windows，但功能等都尚未驗證完成(支援性不佳)。

# 後續 #

ROS系統核心以及有用的工具和函示庫將透過ROS的發行版定期發布。而此發行版會隨著Linux發行版(以Ubuntu為主)，並提供一組可相容軟體供其他人使用和構建。

原始資料出處：http://wiki.ros.org/ROS/Introduction

# 總結 #

雖然這篇文章只能算是翻譯文，但學習每項技術的第一步，總該要先了解開發者的想法、設計概念與往後方向。這樣子在以後自己的開發應用上也會更加確實與容易。

# 重要連結 #
[官方網站](https://www.ros.org/) https://www.ros.org/

[官方維基](http://wiki.ros.org/) http://wiki.ros.org/

維基百科介紹：https://zh.wikipedia.org/wiki/%E6%A9%9F%E5%99%A8%E4%BA%BA%E4%BD%9C%E6%A5%AD%E7%B3%BB%E7%B5%B1
