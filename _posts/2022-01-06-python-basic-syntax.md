---
layout: post #Do not change.
category: [programming, python] #One, more categories or no at all.
title:  "Python 複習筆記-001"
date:   2022-01-06
author: Eric #Author's nick.
---

<a href="/assets/img/posts/pythonlogo.jpg" data-lity class="sx-center">
  <img src="/assets/img/posts/pythonlogo_thumb.jpg"/>
</a>

# 前言 #
Python 的基本語法。   
學習資料：[從零開始學習Python程式設計](https://www.books.com.tw/products/0010738945 "Title")

# 變數 #
Python的儲存資料會以**內建型別**為主。  
Python會以**物件(Object)**來表達資料。  

所以每個物件都具有**身分**、**型別**和**值**；
- 身分(Identity)：每個物件的身分都是獨一無二的！產生之後就無法改變，可以透過內建函式的`id()`來確認。
- 型別(Type)：物件的型別決定了物件要以哪種資料來存放。可以透過內建函式的`type()`來查詢。
- 值(Value)：物件存放的資料，在某些情形下可以改變其值，意指是「**可變(mutable)**」；但有些物件的值宣告之後就「**不可變(immutable)**」。

不同的物件，其型別不同，分配的記憶體空間也會不同。  
為什麼需要記憶體空間？  
主要目的是**暫存資料**，方便做運算。  
如何存放記憶體暫存空間？  
其他程式語言使用「**變數(Variable)**」，它會隨著程式的執行來改變其值。  
Python則是會以「**物件參照(Object reference)**」來存放。  


變數要賦予其名稱，為「**識別字(Identifier)**」之一種。有了識別字名稱後，表示有了「身分」，系統就會配置記憶體空間。  
識別字包含了**變數**、**常數**、**物件**、**類別**、和**方法**等。  
而命名方式必須遵循如下規則；
- 第一個字**必須**是英文字母或者底線。
- 其餘字元可以搭配其他的英文字母或數字。
- 不能使用Python的**關鍵字**或**保留字**來當識別字名稱。
- 對於英文字母的**大小寫**是有所區分的。

Python關鍵字表  

|   continue   | assert  |    and     |  break   |   class   |    def     |    del     |
|:------------:|:-------:|:----------:|:--------:|:---------:|:----------:|:----------:|
|  **lambda**  | **for** | **except** | **else** | **True**  |  **from**  | **return** |
| **nonlocal** | **is**  | **while**  | **try**  | **None**  | **global** | **raise**  |
|  **import**  | **if**  |   **as**   | **elif** | **False** |   **or**   | **yield**  |
| **finally**  | **in**  |  **pass**  | **not**  | **with**  |            |            |

Python使用**動態型別(Dynamics typing)**，使用變數時，只要給予變數和變數值即可。  
動態型別是甚麼意思？  
是指執行程式時，直譯器才會去找所宣告變數的型別。由於識別字的名稱和型別是各自獨立的，所以同一個名稱會依據程式碼不同來指向不同的型別。  

編寫程式碼時，所使用的等號「**=**」並不是數學定義裡的等於，而是「**指派(Assignment)**」；也就是將右邊的值指派左邊的變數。  

Python允許開發者同時指派一個變數，也可以利用「**,**」(分隔變數)以及「**;**」(分隔運算式)連續宣告變數。  

### 變數置換 ###
在其他程式語言的語法中，如果要把兩個變數做**置換(swap)**，通常須借助第三個變數暫存變數。  
不過在Python只須依照下列語法即可；
```
x, y = 10, 20
x, y = y, x
print(x, y)
```
### 連續宣告 ###
Python有可以連續宣告變數的特性，只要使用內建函式`eval()`即可。  
其語法如下：
```
eval(expression, globals=None, locals=None)
```
- expression：字串運算式。
- globals和locals為選擇參數，使用globals參數時必須採用**字典(dict)物件**。而使用locals參數時則要使用**映射類別**。

# 型別 #
物件導向概念淺談：  
**類別(class)**提供物件藍圖，而物件則是將類別實體化。  
類別和物件皆有**屬性**和**方法**，可使用運算子「**.**」(Dot)來存取。  
所以，不管是匯入的**模組**或者是**內建型別**都適用這個概念。  
其語法如下：
```
className.attribute 物件.屬性
className.method() 物件.方法([參數串列])
```
使用類別的屬性或方法時，必須使用**類別名稱**。  

常見的內建型別有以下五類：**數值型別(Numeric Type)**、**序列型別(Sequence Type)**、**迭代型別(Iterator Type)**、**集合型別(Set Type)**、和**映射型別(Mapping Type)**。  

本篇複習會以數值型別為主。  

Python的數值型別皆由標準函式庫所提供，並且皆具有「**不可變**」的特性。  
要查看物件的型別，可以使用`type()`函式，語法如下：
```
type(object)  #檢查宣告變數的型別
```
object：表示所宣告的變數或資料。  

### 整數型別 ###
整數：是指不含小數位數的數值。  
分為**整數(Integer)**和**布林(Boolean)**兩種。  
  
Python並不會像其他語言會區分整數與長整數，所以整數的長度可以「**無窮精確度**」(Unlimited precision)，也就意味著數值無論是大或是小皆依據電腦記憶體容量來呈現。  
數值的字面值(literal)通常以**十進位**(decimal)為主，Python是以內建函式`int()`來表達。  
然在某些特定情形下，則可能需要以**二進位**(Binary)、**八進位**(Octal)、或**十六進位**(Hexadecimal)來表示。  
**整數資料皆屬於類別「int」的實作物件。**  

整數轉換函式  

|   內建函式   |                          說明                           |
|:------------:|:-----------------------------------------------------:|
|   bin(int)   |  將十進位數值轉換成二進位，轉換後的數值會以0b為前綴字元  |
|   oct(int)   |  將十進位數值轉換成八進位，轉換後的數值會以0o為前綴字元  |
|   hex(int)   | 將十進位數值轉換成十六進位，轉換後的數值會以0x為前綴字元 |
| int(s, base) |     將字串s依據base參數提供的進位數轉換成十進位數值     |

如果不想有前綴字元，可以使用內建函式`format()`來轉換。
```
format(value[m format_spec])
```
- value：用來設定格式的值或變數。
- format_spec：指定的格式。
`print()`函式只會輸出**十進位**，要以其他進位來輸出還得經過轉換。  
在使用`input()`函式取得輸入值時，該參數會是**字串**，可以利用`int()`來轉換成整數型別。  

`int()`函式補充：
- 參數可以是字串或整數；
- 會將其他進位的數值，轉為整數；
- 也能將指定字串轉為十進位數值。

布林：為int的子類別。使用`bool()`函式。它只有**True**和**False**兩個值，而一般使用在流程控制做**邏輯判斷**。  
可以使用數值「1」或「0」來表示True或False。  
而以下項目，其布林值會以False回傳：
- 數值為 0。
- 特殊物件為 None。
- 序列和群集資料型別中的空字串、空串列(List)、或空序對(Tuple)。

### 浮點數型別 ###
浮點數：含有小數位數的數值，也就是**實數**。  
分為以下三種資料型別：
- float：內建型別，儲存**倍精度浮點數**(等同**雙精度浮點數**)，它會隨著作業平台來卻精確度範圍，使用`float()`函式表示。
- complex：內建型別，處理**複數**數值資料，也就是由實數(real)和虛數(imaginary)所組成的數值資料。
- decimal：若處理數值時，需要精確的小數位數，可透過標準函式庫的**decimal.Decimal類別**支援。
浮點數除了帶有小數位數值外，也能利用**科學符號**(**指數**)來表示。  

一般處理浮點數都是使用內建函式`float()`，它可以建立浮點數物件，並只接受一個參數。  
此外，它也可以處理三個特殊的浮點數；**正無窮大(Infinity)**、**負無窮大(NegativeInfinity)**、**非數(Not a number, nan)**。其表示方式如下：
```
float("Infinity")  #正無窮大
float("-Infinity") #負無窮大
float("nan")       #非數
```
需使用`import`敘述來匯入模組。而處理數值的模組有：math(由標準模組所提供)。  
math內有以下兩種方法：  
`isnan()`方法可以用來判斷是否為非數(NaN)的資料。  
`isinf()`方法可以用來判斷是否為(正/負)無窮大的資料。  

若想要了解浮點數所支援的小數位數，則要匯入sys模組。利用`float_info`物件提供的`epsilon`屬性作查詢。  

Float的類別方法  

|     方法     |                   說明                   |   備註   |
|:------------:|:--------------------------------------:|:------:|
|  fromhex(s)  |       將十六進位的浮點數轉為十進位       | 物件方法 |
|    hex()     |        以字串來回傳十六進位浮點數        | 類別方法 |
| is_integer() | 判斷是否為整數，若小數位數是零，則回傳True | 類別方法 |

**函式(function)**和**方法(method)**差異  
函式通常泛指其內建函式。  
方法則是由類別或物件所提供。  

內建函式`complex()`則是用來處理複數資料。在表示複數的虛數部分，還得加上字元**j**。其語法如下：
```
comlex(re, im)
```
re為real，表實數；im為imag，表虛數。  

由於complex本身也是類別，可以使用屬性real和imag來取得複數的實數部分或虛數部分。  
`.conjugate()`則是取得共軛複數的方法。  
也可以使用**字串**來建立複數物件，但要注意其格式。  

若想要取得擁有更精確小數位數的數值，就得匯入decimal模組，再使用物件方法`Decimal()`來產生精確數值。  
使用該方法時，可以用浮點數作為其參數。且具有「**有效位數**」特性。  
使用Decimal類別時，它的算術環境會提供各項紀錄的定義，如精確度、捨入規則等。可透過`getccontext()`函式來取得相關紀錄。「**rounding**」屬性則可用來查看數值的捨入規則。  

Rounding的捨入規則：
- ROUND_CEILING：朝著無窮大的方向。
- ROUND_DOWN：朝著接近零的方向，也就是無條件捨去。
- ROUND_FLOOR：朝著負無窮大的方向。
- ROUND_HALF_DOWN：四捨六入，五朝著接近零的方向。
- ROUND_HALF_EVEN：四捨六入，五朝著最接近偶數的方向。
- ROUND_HALF_UP：四捨六入，五朝著遠離零的方向。
- ROUND_UP：朝著遠離零的方向，也就是無條件進位。
- ROUND_05UP：捨去最後位數後，若為零或五則進位，其他數就捨位。

內建函式`round()`可以將小數位數做四捨五入的動作，其語法如下：
```
round(number[, ndigits])
```
- number：欲捨去小數位數的數值。
- ndigits：欲保留的小數位數，省略時會捨去所有的小數位數。

使用算術運算子做**除法**時，若有int與float，所得商數會以**float**型別為主。  
因此不同型別的數值做運算時，其記憶體空間將以下原則設定；
- 型別是**float**和**complex**時，會以**complex**為主。
- 使用**decimal**型別通常是要求有更高的精確度，它會以其它的decimal型別做運算。

### 分數 ###
分數(Fraction)並**不屬於**數值型別。所以分數或稱有理數(Rational Number)是以「分子/分母」這行式來表達。  
若要對分數做運算時，則必須要匯入`fractions`模組。`Fraction()`方法的語法如下：
```
Fraction(numerator, denominator)
```
- numerator：分數中的分子，預設值為 0。
- denominator：分數中的分母，預設值為 1。
- 無論是分子或分母都只能用正值或負值**整數**，否則會發生錯誤。
使用`Fraction()`方法時會自動約分，但參數不能浮點數和整數混合使用，會產生「**型別錯誤**」(TypeError)。  

# 運算 #
所謂的運算式由**運算元(operand)**與**運算子(operator)**組成。
- 運算元：包含了變數、數值和字元。
- 運算子：算術運算子、指派運算子、邏輯運算子和比較運算子等。
運算子如果只有一個運算元，稱為**單一運算子(Unary operator)**。如果有兩個運算元，則是二元運算子。  

### 算術運算子 ###
提供運算元的基本運算，包含加、減、乘、除等等。

| 運算子 |      說明      |
|:------:|:------------:|
|   +    |  把運算元相加  |
|   -    |  把運算元相減  |
|   *    |  把運算元相乘  |
|   /    |  把運算元相除  |
|   **   |   指數運算子   |
|   //   |   取得整除數   |
|   %    | 除法運算取餘數 |

在四則運算時，比較特別的是除法，所得商數是**浮點數**。要取得**整數**商數，可以使用`int()`函式做轉換，或者使用「//」運算子。  
如果是要取得兩個數值相除之後的商數和餘數，使用內建函式`divmod()`。其語法如下：
```
divmod(x, y)
```
- 參數x 執行「x // y」的運算。
- 參數y 執行「x % y」的運算。

使用數值配合算術運算子時，還可以呼叫`math`模組，利用math類別提供的屬性和方法做相關運算應用。

|  屬性、方法  |                 說明                 |
|:-----------:|:-----------------------------------:|
|     pi      |           屬性，提供圓周率            |
|      e      | 屬性，為數學常數，是自然對數函數的底數 |
|   ceil(x)   |  將數值x 無條件進位成正整數或負整數  |
|  floor(x)   |  將數值x 無條件捨去成正整數或負整數  |
|   exp(x)    |          回報e值 **x的結果           |
|   sqrt(x)   |            計算x的平方根             |
|  pow(x, y)  |            計算x的y冪次方            |
| fmod(x, y)  |           計算x % y的餘數            |
| hypot(x, y) |          同sqrt(x*x + y*y)           |
|  gcd(a, b)  |     回傳a、b兩個數值的最大公因數      |
|  isnan(x)   |      回傳布林值True，表示它是NaN      |
|  isinf(x)   |      回傳布林值True，表示它是Inf      |

比較  
使用math類別提供的`pow()`方法時，它有兩個參數：x, y；  
而內建函式`pow()`時，則會有三個參數，其語法如下：
```
pow(x, y[, z])
```
參數z 是用來求取餘數。若省略的話，就會跟math類別提供的方法相同。  

### 指派運算子 ###
配合算術運算子，以變數為運算元時，可以把運算後的結果再指派給變數本身。  

| 運算子 |        運算        |  指派運算   |
|:------:|:------------------:|:-----------:|
|   +=   | total = total + 5  | total += 5  |
|   -=   | total = total - 5  | total -= 5  |
|   ＊＝   | total = total * 5  | total *= 5  |
|   /=   | total = total / 5  | total /= 5  |
|  ＊＊＝   | total = total ** 5 | total **= 5 |
|  //=   | total = total // 5 | total //= 5 |
|   %=   | total = total % 5  | total %= 5  |

### 比較運算子 ###
比較運算子通常是用來比較兩個運算元的**大小**，所得到的結果會以布林值True或False回傳。  

| 運算子 |    運算    | 結果  |            說明            |
|:------:|:----------:|:-----:|:------------------------:|
|   >    | opA > opB  | True  |    opA大於opB，回傳True     |
|   <    | opA < opB  | False |    opA小於opB，回傳Flase    |
|   >=   | opA >= opB | True  | opA大於或等於opB，回傳True  |
|   <=   | opA <= opB | False | opA小於或等於opB，回傳False |
|   ==   | opA == opB | False |    opA等於opB，回傳False    |
|   !=   | opA != opB | True  |   opA不等於opB，回傳True    |

### 邏輯運算子 ###
邏輯運算子是針對運算式的True、False值做邏輯判斷。  

| 運算子  | 運算式1 | 運算式2 | 結果  |               說明                |
|:------:|:-------:|:-------:|:-----:|:-------------------------------:|
| and(且) |  true   |  true   | true  |   兩邊運算式為true，才會回傳true   |
| and(且) |  true   |  false  | flase |   兩邊運算式為true，才會回傳true   |
| and(且) |  false  |  true   | false |   兩邊運算式為true，才會回傳true   |
| and(且) |  false  |  false  | false |   兩邊運算式為true，才會回傳true   |
| or(或)  |  true   |  true   | true  | 只要一邊運算式為true，就會回傳true |
| or(或)  |  true   |  false  | true  | 只要一邊運算式為true，就會回傳true |
| or(或)  |  false  |  true   | true  | 只要一邊運算式為true，就會回傳true |
| or(或)  |  false  |  false  | false | 只要一邊運算式為true，就會回傳true |
| not(否) |  true   |   --    | false |   運算式反向，所得結果與原來相反   |
| not(否) |  false  |   --    | true  |   運算式反向，所得結果與原來相反   |

通常邏輯運算子會與流程控制配合使用。and, or運算子做邏輯運算時會採用「快捷」(Short-circuit)運算，當運算元非布林值時，直接回傳運算元。  

### 位元運算子 ###
位元(Bitwise)運算會以二進位(基底為2)為運算式。  

| 運算子 | 運算式1 | 運算式2 | 結果 |                  說明                  |
|:------:|:-------:|:-------:|:----:|:------------------------------------:|
| &(and) |    1    |    1    |  1   |   運算元1、運算元2的值皆為1，才會回傳1   |
| &(and) |    1    |    0    |  0   |   運算元1、運算元2的值皆為1，才會回傳1   |
| &(and) |    0    |    1    |  0   |   運算元1、運算元2的值皆為1，才會回傳1   |
| &(and) |    0    |    0    |  0   |   運算元1、運算元2的值皆為1，才會回傳1   |
| ｜(Or)  |    1    |    1    |  1   | 運算元1、運算元2的值有一個為1，就會回傳1 |
| ｜(Or)  |    1    |    0    |  1   | 運算元1、運算元2的值有一個為1，就會回傳1 |
| ｜(Or)  |    0    |    1    |  1   | 運算元1、運算元2的值有一個為1，就會回傳1 |
| ｜(Or)  |    0    |    0    |  0   | 運算元1、運算元2的值有一個為1，就會回傳1 |
| ^(Xor) |    1    |    1    |  1   |   運算元1、運算元2的值不同，才會回傳1    |
| ^(Xor) |    1    |    0    |  1   |   運算元1、運算元2的值不同，才會回傳1    |
| ^(Xor) |    0    |    1    |  1   |   運算元1、運算元2的值不同，才會回傳1    |
| ^(Xor) |    0    |    0    |  0   |   運算元1、運算元2的值不同，才會回傳1    |
| ~(not) |    1    |   --    |  0   |       反向運算，將1變成0，將0變成1       |
| ~(not) |    0    |   --    |  1   |       反向運算，將1變成0，將0變成1       |

**特殊位元運算子**  

|  運算子  |        語法        |                      說明                       |
|:------:|:----------------:|:---------------------------------------------:|
| <<(左移) | 運算元1 << 運算元2 | 將運算元1依運算元2指定的位元數向左移動，右邊補零 |
| >>(右移) | 運算元1 >> 運算元2 | 將運算元1依運算元2指定的位元數向右移動，左邊補零 |
