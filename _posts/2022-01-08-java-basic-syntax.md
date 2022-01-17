---
layout: post #Do not change.
category: [programming, java] #One, more categories or no at all.
title:  "Java 複習筆記-001"
date:   2022-01-08
author: Eric #Author's nick.
---

<a href="/assets/img/posts/javalogo.jpg" data-lity class="sx-center">
  <img src="/assets/img/posts/javalogo_thumb.jpg"/>
</a>

# 前言 #
Java 的基本語法。  
學習資料：[Java教學手冊](https://www.books.com.tw/products/0010555220 "Title")

# 程式碼解析 #
Java的註解是以「**//**」記號開始，至該行結束來表示註解的文字。而「//」所影響到的範圍，僅僅是在它之後的同一行敘述。  
**public**與**class**是Java的關鍵字(keyword)。  
class為「**類別**」之意，後面接上類別之名。  
public則是用來表示該類別為**共有**，也就是在整個程式裡都可以存取到它。  
如果將一個類別宣告成public，就必須將檔案名稱命名為這個類別的名稱。也就是說，在一個附加檔名為.java的檔案裡**只能有一個**public類別，否則檔案便無法命名，此為Java的特殊規定。  

`main()`在Java裡是一個相當特殊的函數，他一定要宣告成public，使得在類別的其他地方可以呼叫到它。另外，由於`main()`沒有回傳值，所以之前要加上void。最後，static是把`main()`宣告成「**類別函數**」，使得在程式一啟動時，便可以自動的執行`main()`。  
`main()`括號內之引數`String arg[]`表示程式執行時，所鍵入的引數(argument)會由**字串型態**的**陣列**arg[]來存放。  

Java把解決特定功能的模組稱為「**方法**」(method)，相等於C語言裡的函數(function)。  

`main()`的主體(body)均由左大括號({)到右大括號(})為止。  
每一個獨立的Java程式一定要有`main()`才能執行。  

Java有別於其他直譯式語言，使用變數之前**必須**宣告其形態。  

`System.out`是指標準輸出，而接續在它後面的文字`println`，是由print與line所組成的縮寫，其意義是將後面括號中的內容列印於標準輸出設備上後，並將游標移到下一行的開端。若不用換行，可改用`print`。  

# 類別 #
Java程式是由**類別(class)**所組成。而類別的內容必須放置在左大括號(})與右大括號(})內。  

public是Java的關鍵字外，也是類別、成員的**修飾子(modifier)**，指的是對於類別的存取方式為共有。  

由於Java程式是由類別所組成，因此在完整的Java程式裡，至少需要有一個類別。因此，其原始程式的檔名不能隨意命名，必須和public類別名稱一樣。所以，在一個獨立的原始程式裡，只能有一個public類別，但可以有數個「非public」類別。如果在原始程式檔案中，沒有一個類別是public，那麼該原始程式的檔名就可以不必和類別名稱相同。  

Java程式是由一個或一個以上的類別組合而成，其中程式執行的起點為`main()`函數，它必須撰寫在public的類別之內。  
Java的`main()`類似於C語言的主函數`main()`。所以Java的`main()`也是程式執行的開端，而且每一個Java程式必須有一個`main()`，並且**只能有一個**。  
最後，`main()`之前還必須冠上public static void這三個修飾子。  

# 變數 #
變數在程式語言中都扮演著最基本的角色。因為它可以用來存放資料，而Java在使用變數之前也必須先宣告它所欲儲存的資料型態。  

(1)宣告  
其敘述如下：  
```int num; // 宣告 num 為整數變數```  
int為Java的關鍵字，代表整數的宣告。如果想同時宣告數個整數變數，除了可以像上面的敘述一樣分別宣告它們外，也可以把它們都寫在同一個敘述中，再將每個變數以逗號(,)分開，其敘述如下：  
```int num, num1, num2; // 同時宣告num, num1, num2為整數變數```  

(2)資料型態  
除了整數型態之外，Java還有**長整數(long)**、**短整數(short)**、**浮點數(float)**、**倍精度浮點數(double)**、**字元(char)** 和 **字串(String)** 等資料型態。  

(3)名稱和其限制  
依個人喜好來決定變數的名稱，但不能用到Java的關鍵字，不過通常會以其所代表的意義來取名。  
變數名稱可以使用英文字母、數字或底線。但要注意的是，名稱中不能有空白字元，且第一個字元不能是**數字**。  
此外，Java的變數名稱是有大小寫之別。  

# 設值 #
Java變數設值的方式是把等號(＝)右邊的值設定給左邊的變數存放。還有，一眼便能看出其內容的數值稱為「字面值」(literal)。也就是說，把等號右邊的字面值設定給等號左邊的變數存放。而有三種設定方式：  
1. 在宣告的時候設值  
2. 宣告後再設值  
3. 在程式中適當的位置宣告變數並設值  

# 輸出 #
敘述如下：  
``` System.out.println("Hello Java");```  
左右括號之間的內容，就是欲顯示在螢幕上的內容，稱之為**引數**，引數可以是字元、字串、數值或是運算式，引數與引數之間使用加號(＋)做為區隔。而在`println()`中若要印出的是字串型態時，則必須以一對雙引號(")包圍住字串，若要印出的是變數的值，則直接將變數名稱填入即可。前述提到可用加號(＋)在引數與引數之間做區隔，較多的使用意義是「合併、連接」。  

# 有引數的main()函數 #
常見`main()`的引數多為`String agr[]`。而`String agr[]`有甚麼意義？其實，`arg[]`是用接收傳入程式的引數，此時arg[0]
會存放第一個引數，arg[1]會存放第二個引數，依此類推。而這些引數的型態皆為String(字串型態)。  

Java裡最基本的元件：**識別字**及**關鍵字**。  

# 識別字 #
在Java中，變數、類別或者是函數的名稱視為識別字，它們是開發者自行定義的文字，由英文大小寫字母、數字或底線組合而成。  
識別字名稱不能使用到Java的關鍵字，同時，識別字的第一個字元，必須是英文字母或是底線，數字只能在第二個字元之後出現；而空白字元及特殊符號，則不能出現在識別字的名稱裡。此外，Java對於識別字是有大小寫之別。  
Java有識別字的命名習慣原則  

| 識別字 | 命名原則                                                                                                                      |
|:----:|:--------------------------------------------------------------------------------------------------------------------------|
|  常數  | 常數是指設值之後，便無法修改其值的變數。全部字元皆由英文大寫字母及底線組成                                                      |
|  變數  | 英文小寫字母開始，若由數個英文單字組成，則後面的英文字由大寫起頭，其餘小寫                                                       |
|  函數  | 英文小寫字母開始，若由數個英文單字組成，則後面的英文字由大寫起頭，其餘小寫。函數和變數的命名方式相同，不同的是函數名稱後面會加上() |
|  類別  | 英文大寫字母開始，若由數個英文單字組成，則後面的英文字由大寫起頭，其餘小寫                                                       |

最後，Java沒有限定識別字的長度。  

# 關鍵字 #
識別字是開發者用來命名變數或者是函數的文字；關鍵字則是編譯程式本身所使用的識別字。  
開發者不能更改或者是重複定義關鍵字。因此，自行定義的函數或者是變數名稱都不能與Java的關鍵字相同。  

Java常用關鍵字  

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
