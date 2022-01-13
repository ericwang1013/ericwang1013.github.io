---
layout: post #Do not change.
category: [programming, compare] #One, more categories or no at all.
title:  "基本語法比較之二"
date:   2022-01-13
author: Eric #Author's nick.
---

# 前言 #
基本語法之二：是各語言的識別字和關鍵字統整。

# 識別字 #
C 語言，變數與函數的名稱均是識別字。  
C++ ，變數、函數或者是類別的名稱均為識別字。  
C++ 識別字的命名習慣原則  

| 識別字 |                                命名原則                                 |
|:----:|:-------------------------------------------------------------------:|
|  常數  |                   全部字元皆由英文大寫字母及底線組成                    |
|  變數  | 英文小寫字母開始，若由數個英文單字組成，則後面的英文字由大寫起頭，其餘小寫 |
|  函數  | 英文小寫字母開始，若由數個英文單字組成，則後面的英文字由大寫起頭，其餘小寫 |
|  類別  | 英文大寫字母開始，若由數個英文單字組成，則後面的英文字由大寫起頭，其餘小寫 |

Java ，變數、類別或者是函數的名稱均為識別字。  
Java 識別字的命名習慣原則  

| 識別字 | 命名原則                                                                                                                      |
|:----:|:--------------------------------------------------------------------------------------------------------------------------|
|  常數  | 常數是指設值之後，便無法修改其值的變數。全部字元皆由英文大寫字母及底線組成                                                      |
|  變數  | 英文小寫字母開始，若由數個英文單字組成，則後面的英文字由大寫起頭，其餘小寫                                                       |
|  函數  | 英文小寫字母開始，若由數個英文單字組成，則後面的英文字由大寫起頭，其餘小寫。函數和變數的命名方式相同，不同的是函數名稱後面會加上() |
|  類別  | 英文大寫字母開始，若由數個英文單字組成，則後面的英文字由大寫起頭，其餘小寫                                                       |

Python ，變數、常數、物件、類別和方法均為識別字。  

# 關鍵字 #
關鍵字是編譯程式本身所使用的識別字。自行定義的變數或函數的名稱等都不能與各語言的關鍵字相同。  
C 語言關鍵字表  

|     auto     |    break    |     case     |    char    |    const     |
|:------------:|:-----------:|:------------:|:----------:|:------------:|
| **continue** | **default** | **defined**  |   **do**   |  **double**  |
|   **else**   |  **enum**   |  **extern**  | **float**  |   **for**    |
|   **goto**   |   **if**    |   **int**    |  **long**  | **register** |
|  **return**  |  **short**  |  **signed**  | **sizeof** |  **static**  |
|  **struct**  | **switch**  | **typedef**  | **union**  | **unsigned** |
|   **void**   |  **while**  | **volatile** |            |              |

C++ 關鍵字表  

|       asm        |     auto     |         bool         |      break      |      case      |
|:----------------:|:------------:|:--------------------:|:---------------:|:--------------:|
|    **catch**     |   **char**   |      **class**       |    **const**    | **const_cast** |
|   **continue**   | **default**  |      **delete**      |     **do**      |   **double**   |
| **dynamic_cast** |   **else**   |       **enum**       |  **explicit**   |   **extern**   |
|    **false**     |  **float**   |       **for**        |   **friend**    |    **goto**    |
|      **if**      |  **inline**  |       **int**        |    **long**     |  **mutable**   |
|  **namespace**   |   **new**    |     **operator**     |   **private**   | **protected**  |
|    **public**    | **register** | **reinterpret_cast** |   **return**    |   **short**    |
|   **signeded**   |  **sizeof**  |      **static**      | **static_cast** |   **struct**   |
|     **try**      | **typedef**  |       **this**       |    **throw**    |    **true**    |
|   **unsigned**   |  **using**   |     **virtual**      |    **void**     |  **volatile**  |
|   **wchart_t**   |  **while**   |                      |                 |                |

Java 關鍵字表  

|    abstract    |    boolean    |    break     |       byte       |     case     |
|:--------------:|:-------------:|:------------:|:----------------:|:------------:|
|   **catch**    |   **char**    |  **class**   |    **const**     |  **false**   |
|  **continue**  |  **default**  |    **do**    |    **double**    |   **else**   |
|  **extends**   |   **final**   | **finally**  |    **float**     |   **for**    |
|    **goto**    |    **if**     |  **import**  |  **implements**  |   **int**    |
| **instanceof** | **interface** |   **long**   |    **native**    |   **new**    |
|    **null**    |  **package**  | **private**  |  **protected**   |  **public**  |
|   **return**   |   **short**   |  **static**  | **synchronized** |  **super**   |
|    **this**    |   **throw**   |  **throws**  |  **transient**   |   **true**   |
|    **try**     |   **void**    | **volatile** |    **while**     | **strictfp** |
|   **switch**   |               |              |                  |              |

Python 關鍵字表  

|   continue   | assert  |    and     |  break   |   class   |    def     |    del     |
|:------------:|:-------:|:----------:|:--------:|:---------:|:----------:|:----------:|
|  **lambda**  | **for** | **except** | **else** | **True**  |  **from**  | **return** |
| **nonlocal** | **is**  | **while**  | **try**  | **None**  | **global** | **raise**  |
|  **import**  | **if**  |   **as**   | **elif** | **False** |   **or**   | **yield**  |
| **finally**  | **in**  |  **pass**  | **not**  | **with**  |            |            |

# 總結 #
將四種語言的基本語法作了比較，想當然爾，C 和 C++ 是最為相似的，但 Java 也是有諸多相近之處。而 Python 就真與三大前輩語言有太多差異了。  
不過本著重於多數教科書所編寫內容之比較，必會有遺漏之點，在之後應用就要自行注意。  
