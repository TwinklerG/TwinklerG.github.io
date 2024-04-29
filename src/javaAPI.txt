# Number类

基础数据类型：byte、int、short、long、double、float、boolean、char；

对应包装类型：Byte、Integer、Short、Long、Double、Float、Character、Boolean;

编译器会自动的将基本数据类型装箱成对象类型，或者将对象类型拆箱成基本数据类型。如下

```java
public static void main(String[] args) {
	int num1 = 1;
	//将基本数据类型装箱成对象包装类型
	Integer num2 = num1;
	Integer num3 = 3;
	//将对象数据类拆箱
	int num4 = num3;
}
```

# Math类

基本数学运算的属性和方法（均为static形式）

```java
public class Test {  
    public static void main (String []args)  
    {  
        System.out.println("90 度的正弦值：" + Math.sin(Math.PI/2));  
        System.out.println("0度的余弦值：" + Math.cos(0));  
        System.out.println("60度的正切值：" + Math.tan(Math.PI/3));  
        System.out.println("1的反正切值： " + Math.atan(1));  
        System.out.println("π/2的角度值：" + Math.toDegrees(Math.PI/2));  
        System.out.println(Math.PI);  
    }  
}
```

## Number & Math 类方法

下面的表中列出的是常用的 Number 类和 Math 类的方法：

| 序号 | 方法与描述                                                   |
| :--- | :----------------------------------------------------------- |
| 1    | [xxxValue()](https://www.w3cschool.cn/java/number-xxxvalue.html) 将number对象转换为xxx数据类型的值并返回。 |
| 2    | [compareTo() ](https://www.w3cschool.cn/java/number-compareto.html)将number对象与参数比较。 |
| 3    | [equals()](https://www.w3cschool.cn/java/number-equals.html) 判断number对象是否与参数相等。 |
| 4    | [valueOf() ](https://www.w3cschool.cn/java/number-valueof.html)返回一个Integer对象指定的内置数据类型 |
| 5    | [toString() ](https://www.w3cschool.cn/java/number-tostring.html)以字符串形式返回值。 |
| 6    | [parseInt() ](https://www.w3cschool.cn/java/number-parseint.html)将字符串解析为int类型。 |
| 7    | [abs() ](https://www.w3cschool.cn/java/number-abs.html)返回参数的绝对值。 |
| 8    | [ceil() ](https://www.w3cschool.cn/java/number-ceil.html)返回大于等于( >= )给定参数的的最小整数，类型为双精度浮点型。 |
| 9    | [floor() ](https://www.w3cschool.cn/java/number-floor.html)返回小于等于（<=）给定参数的最大整数 。 |
| 10   | [rint() ](https://www.w3cschool.cn/java/number-rint.html)返回与参数最接近的整数。返回类型为double。 |
| 11   | [round() ](https://www.w3cschool.cn/java/number-round.html)返回一个最接近的int、long型值。 |
| 12   | [min() ](https://www.w3cschool.cn/java/number-min.html)返回两个参数中的最小值。 |
| 13   | [max() ](https://www.w3cschool.cn/java/number-max.html)返回两个参数中的最大值。 |
| 14   | [exp() ](https://www.w3cschool.cn/java/number-exp.html)返回自然数底数e的参数次方。 |
| 15   | [log() ](https://www.w3cschool.cn/java/number-log.html)返回参数的自然数底数的对数值。 |
| 16   | [pow() ](https://www.w3cschool.cn/java/number-pow.html)返回第一个参数的第二个参数次方。 |
| 17   | [sqrt() ](https://www.w3cschool.cn/java/number-sqrt.html)求参数的算术平方根。 |
| 18   | [sin() ](https://www.w3cschool.cn/java/number-sin.html)求指定double类型参数的正弦值。 |
| 19   | [cos() ](https://www.w3cschool.cn/java/number-cos.html)求指定double类型参数的余弦值。 |
| 20   | [tan() ](https://www.w3cschool.cn/java/number-tan.html)求指定double类型参数的正切值。 |
| 21   | [asin()](https://www.w3cschool.cn/java/number-asin.html) 求指定double类型参数的反正弦值。 |
| 22   | [acos() ](https://www.w3cschool.cn/java/number-acos.html)求指定double类型参数的反余弦值。 |
| 23   | [atan() ](https://www.w3cschool.cn/java/number-atan.html)求指定double类型参数的反正切值。 |
| 24   | [atan2()](https://www.w3cschool.cn/java/number-atan2.html) 将笛卡尔坐标转换为极坐标，并返回极坐标的角度值。 |
| 25   | [toDegrees()](https://www.w3cschool.cn/java/number-todegrees.html) 将参数转化为角度。 |
| 26   | [toRadians() ](https://www.w3cschool.cn/java/number-toradians.html)将角度转换为弧度。 |
| 27   | [random()](https://www.w3cschool.cn/java/number-random.html) 返回一个随机数。 |

# Character类

将一个 char 类型的参数传递给需要一个 Character 类型参数时，那么编译器会自动地将 char 类型参数转换为 Character 对象。 这种特征称为装箱，反过来称为拆箱。

```java
// Here following primitive char 'a'
// is boxed into the Character object ch
Character ch = 'a';

// Here primitive 'x' is boxed for method test,
// return is unboxed to char 'c'
char c = test('x');
```

## 转义序列

Java 的转义序列：

| 转义序列 | 描述                     |
| :------- | :----------------------- |
| \t       | 在文中该处插入一个tab键  |
| \b       | 在文中该处插入一个后退键 |
| \n       | 在文中该处换行           |
| \r       | 在文中该处插入回车       |
| \f       | 在文中该处插入换页符     |
| \\'      | 在文中该处插入单引号     |
| \\\"     | 在文中该处插入双引号     |
| \\\      | 在文中该处插入反斜杠     |

## Character 方法

下面是 Character 类的方法：

| 序号 | 方法与描述                                         |
| :--- | :------------------------------------------------- |
| 1    | isLetter() 是否是一个字母                          |
| 2    | isDigit() 是否是一个数字字符                       |
| 3    | isWhitespace() 是否一个空格                        |
| 4    | isUpperCase() 是否是大写字母                       |
| 5    | isLowerCase() 是否是小写字母                       |
| 6    | toUpperCase() 指定字母的大写形式                   |
| 7    | toLowerCase() 指定字母的小写形式                   |
| 8    | toString() 返回字符的字符串形式，字符串的长度仅为1 |

# String类

string类有11中构造方法。

如下合法

```java
char[] tex = {'H','e','l','l','o'};
String helloString = new String(tex);
```

String类==不可变==，如果要对字符串修改，应该使用**StringBuffer** & **StringBuilder** 类。

## 字符串长度

`s.length()`

## 连接字符串

`string1.concat(string2)`或者直接`string1 + string2`

## 创建格式化字符串

String 类使用静态方法 format() 返回一个 String 对象。

String 类的静态方法 format() 能用来创建可复用的格式化字符串，而不仅仅是用于一次打印输出。如下所示：

```java
System.out.printf("The value of the float variable is " +
                  "%f, while the value of the integer " +
                  "variable is %d, and the string " +
                  "is %s", floatVar, intVar, stringVar);
```

你也可以这样写

```java
String fs;
fs = String.format("The value of the float variable is " +
                   "%f, while the value of the integer " +
                   "variable is %d, and the string " +
                   "is %s", floatVar, intVar, stringVar);
System.out.println(fs);
```

## String 方法

下面是 String 类支持的常用方法，更多详细，参看 Java API 文档:

| SN(序号) | 方法描述                                                     |
| :------- | :----------------------------------------------------------- |
| 1        | [char charAt(int index) ](https://www.w3cschool.cn/java/java-string-charat.html)返回指定索引处的 char 值。 |
| 2        | [int compareTo(Object o) ](https://www.w3cschool.cn/java/java-string-compareto.html)把这个字符串和另一个对象比较。 |
| 3        | [int compareTo(String anotherString) ](https://www.w3cschool.cn/java/java-string-compareto.html)按字典顺序比较两个字符串。 |
| 4        | [int compareToIgnoreCase(String str) ](https://www.w3cschool.cn/java/java-string-comparetoignorecase.html)按字典顺序比较两个字符串，不考虑大小写。 |
| 5        | [String concat(String str) ](https://www.w3cschool.cn/java/java-string-concat.html)将指定字符串连接到此字符串的结尾。 |
| 6        | [boolean contentEquals(StringBuffer sb) ](https://www.w3cschool.cn/java/java-string-contentequals.html)当且仅当字符串与指定的StringButter有相同顺序的字符时候返回真。 |
| 7        | [static String copyValueOf(char[] data) ](https://www.w3cschool.cn/java/java-string-copyvalueof.html)返回指定数组中表示该字符序列的 String。 |
| 8        | [static String copyValueOf(char[] data, int offset, int count) ](https://www.w3cschool.cn/java/java-string-copyvalueof.html)返回指定数组中表示该字符序列的 String。 |
| 9        | [boolean endsWith(String suffix)](https://www.w3cschool.cn/java/java-string-endswith.html) 测试此字符串是否以指定的后缀结束。 |
| 10       | [boolean equals(Object anObject) ](https://www.w3cschool.cn/java/java-string-equals.html)将此字符串与指定的对象比较。 |
| 11       | [boolean equalsIgnoreCase(String anotherString) ](https://www.w3cschool.cn/java/java-string-equalsignorecase.html)将此 String 与另一个 String 比较，不考虑大小写。 |
| 12       | [byte[] getBytes() ](https://www.w3cschool.cn/java/java-string-getbytes.html) 使用平台的默认字符集将此 String 编码为 byte 序列，并将结果存储到一个新的 byte 数组中。 |
| 13       | [byte[] getBytes(String charsetName) ](https://www.w3cschool.cn/java/java-string-getbytes.html)使用指定的字符集将此 String 编码为 byte 序列，并将结果存储到一个新的 byte 数组中。 |
| 14       | void getChars(int srcBegin, int srcEnd, char[] dst, int dstBegin) 将字符从此字符串复制到目标字符数组。 |
| 15       | [int hashCode() ](https://www.w3cschool.cn/java/java-string-hashcode.html)返回此字符串的哈希码。 |
| 16       | [int indexOf(int ch) ](https://www.w3cschool.cn/java/java-string-indexof.html)返回指定字符在此字符串中第一次出现处的索引。 |
| 17       | [int indexOf(int ch, int fromIndex) ](https://www.w3cschool.cn/java/java-string-indexof.html)返回在此字符串中第一次出现指定字符处的索引，从指定的索引开始搜索。 |
| 18       | [int indexOf(String str) ](https://www.w3cschool.cn/java/java-string-indexof.html) 返回指定子字符串在此字符串中第一次出现处的索引。 |
| 19       | [int indexOf(String str, int fromIndex) ](https://www.w3cschool.cn/java/java-string-indexof.html)返回指定子字符串在此字符串中第一次出现处的索引，从指定的索引开始。 |
| 20       | [String intern() ](https://www.w3cschool.cn/java/java-string-intern.html) 返回字符串对象的规范化表示形式。 |
| 21       | [int lastIndexOf(int ch) ](https://www.w3cschool.cn/java/java-string-lastindexof.html) 返回指定字符在此字符串中最后一次出现处的索引。 |
| 22       | [int lastIndexOf(int ch, int fromIndex) ](https://www.w3cschool.cn/java/java-string-lastindexof.html)返回指定字符在此字符串中最后一次出现处的索引，从指定的索引处开始进行反向搜索。 |
| 23       | [int lastIndexOf(String str) ](https://www.w3cschool.cn/java/java-string-lastindexof.html)返回指定子字符串在此字符串中最右边出现处的索引。 |
| 24       | [int lastIndexOf(String str, int fromIndex) ](https://www.w3cschool.cn/java/java-string-lastindexof.html) 返回指定子字符串在此字符串中最后一次出现处的索引，从指定的索引开始反向搜索。 |
| 25       | [int length() ](https://www.w3cschool.cn/java/java-string-length.html)返回此字符串的长度。 |
| 26       | [boolean matches(String regex) ](https://www.w3cschool.cn/java/java-string-matches.html)告知此字符串是否匹配给定的正则表达式。 |
| 27       | [boolean regionMatches(boolean ignoreCase, int toffset, String other, int ooffset, int len) ](https://www.w3cschool.cn/java/java-string-regionmatches.html)测试两个字符串区域是否相等。 |
| 28       | [boolean regionMatches(int toffset, String other, int ooffset, int len) ](https://www.w3cschool.cn/java/java-string-regionmatches.html)测试两个字符串区域是否相等。 |
| 29       | [String replace(char oldChar, char newChar) ](https://www.w3cschool.cn/java/java-string-replace.html)返回一个新的字符串，它是通过用 newChar 替换此字符串中出现的所有 oldChar 得到的。 |
| 30       | [String replaceAll(String regex, String replacement ](https://www.w3cschool.cn/java/java-string-replaceall.html)使用给定的 replacement 替换此字符串所有匹配给定的正则表达式的子字符串。 |
| 31       | [String replaceFirst(String regex, String replacement) ](https://www.w3cschool.cn/java/java-string-replacefirst.html) 使用给定的 replacement 替换此字符串匹配给定的正则表达式的第一个子字符串。 |
| 32       | [String[\] split(String regex) ](https://www.w3cschool.cn/java/java-string-split.html)根据给定正则表达式的匹配拆分此字符串。 |
| 33       | [String[\] split(String regex, int limit) ](https://www.w3cschool.cn/java/java-string-split.html)根据匹配给定的正则表达式来拆分此字符串。 |
| 34       | [boolean startsWith(String prefix) ](https://www.w3cschool.cn/java/java-string-startswith.html)测试此字符串是否以指定的前缀开始。 |
| 35       | [boolean startsWith(String prefix, int toffset) ](https://www.w3cschool.cn/java/java-string-startswith.html)测试此字符串从指定索引开始的子字符串是否以指定前缀开始。 |
| 36       | [CharSequence subSequence(int beginIndex, int endIndex) ](https://www.w3cschool.cn/java/java-string-subsequence.html) 返回一个新的字符序列，它是此序列的一个子序列。 |
| 37       | [String substring(int beginIndex) ](https://www.w3cschool.cn/java/java-string-substring.html)返回一个新的字符串，它是此字符串的一个子字符串。 |
| 38       | [String substring(int beginIndex, int endIndex) ](https://www.w3cschool.cn/java/java-string-substring.html)返回一个新字符串，它是此字符串的一个子字符串。 |
| 39       | [char[\] toCharArray() ](https://www.w3cschool.cn/java/java-string-tochararray.html)将此字符串转换为一个新的字符数组。 |
| 40       | [String toLowerCase() ](https://www.w3cschool.cn/java/java-string-tolowercase.html)使用默认语言环境的规则将此 String 中的所有字符都转换为小写。 |
| 41       | [String toLowerCase(Locale locale) ](https://www.w3cschool.cn/java/java-string-tolowercase.html) 使用给定 Locale 的规则将此 String 中的所有字符都转换为小写。 |
| 42       | [String toString() ](https://www.w3cschool.cn/java/java-string-tostring.html) 返回此对象本身（它已经是一个字符串！）。 |
| 43       | [String toUpperCase() ](https://www.w3cschool.cn/java/java-string-touppercase.html)使用默认语言环境的规则将此 String 中的所有字符都转换为大写。 |
| 44       | [String toUpperCase(Locale locale) ](https://www.w3cschool.cn/java/java-string-touppercase.html)使用给定 Locale 的规则将此 String 中的所有字符都转换为大写。 |
| 45       | [String trim() ](https://www.w3cschool.cn/java/java-string-trim.html)返回字符串的副本，忽略前导空白和尾部空白。 |
| 46       | [static String valueOf(primitive data type x) ](https://www.w3cschool.cn/java/java-string-valueof.html)返回给定data type类型x参数的字符串表示形式。 |

# StringBuffer类和StringBuilder类

和String类不同的是，StringBuffer 和 StringBuilder 类的对象能够被多次的修改，并且不产生新的未使用对象。

> StringBuilder 类在 Java 5 中被提出，它和 StringBuffer 之间的最大不同在于 StringBuilder 的方法不是线程安全的（线程安全就是多线程访问时，采用了加锁机制，当一个线程访问该类的某个数据时，进行保护，其他线程不能进行访问直到该线程读取完，其他线程才可使用。不会出现数据不一致或者数据污染。线程不安全就是不提供数据访问保护，有可能出现多个线程先后更改数据造成所得到的数据是脏数据）。
>
> 由于 StringBuilder 相较于 StringBuffer 有速度优势，所以多数情况下建议使用 StringBuilder 类。然而在应用程序要求线程安全的情况下，则必须使用 StringBuffer 类。

## StringBuffer 方法

以下是 StringBuffer 类支持的主要方法：

| 序号 | 方法描述                                                     |
| :--- | :----------------------------------------------------------- |
| 1    | public StringBuffer append(String s) 将指定的字符串追加到此字符序列。 |
| 2    | public StringBuffer reverse()  将此字符序列用其反转形式取代。 |
| 3    | public delete(int start, int end) 移除此序列的子字符串中的字符。==左闭右开== |
| 4    | public insert(int index, int i) 将 `int` 参数的字符串表示形式插入此序列中。 |
| 5    | replace(int start, int end, String str) 使用给定 `String` 中的字符替换此序列的子字符串中的字符。==左闭右开== |

下面的列表里的方法和 String 类的方法类似：

| 序号 | 方法描述                                                     |
| ---- | ------------------------------------------------------------ |
| 1    | int capacity() 返回当前容量。                                |
| 2    | char charAt(int index) 返回此序列中指定索引处的 `char` 值。  |
| 3    | void ensureCapacity(int minimumCapacity) 确保容量至少等于指定的最小值。 |
| 4    | void getChars(int srcBegin, int srcEnd, char[] dst, int dstBegin) 将字符从此序列复制到目标字符数组 `dst`。 |
| 5    | int indexOf(String str) 返回第一次出现的指定子字符串在该字符串中的索引。 |
| 6    | int indexOf(String str, int fromIndex) 从指定的索引处开始，返回第一次出现的指定子字符串在该字符串中的索引。 |
| 7    | int lastIndexOf(String str) 返回最右边出现的指定子字符串在此字符串中的索引。 |
| 8    | int lastIndexOf(String str, int fromIndex) 返回最后一次出现的指定子字符串在此字符串中的索引。 |
| 9    | int length()  返回长度（字符数）。                           |
| 10   | void setCharAt(int index, char ch) 将给定索引处的字符设置为 `ch`。 |
| 11   | void setLength(int newLength) 设置字符序列的长度。           |
| 12   | CharSequence subSequence(int start, int end) 返回一个新的字符序列，该字符序列是此序列的子序列。 |
| 13   | String substring(int start) 返回一个新的 `String`，它包含此字符序列当前所包含的字符子序列。 |
| 14   | String substring(int start, int end) 返回一个新的 `String`，它包含此序列当前所包含的字符子序列。 |
| 15   | String toString() 返回此序列中数据的字符串表示形式。         |

> CharSequence描述是一个字符串

# Arrays 类

java.util.Arrays 类能方便地操作数组，它提供的所有方法都是静态的。具有以下功能：

- 给数组赋值：通过 fill 方法。
- 对数组排序：通过 sort 方法,按升序。
- 比较数组：通过 equals 方法比较数组中元素值是否相等。
- 查找数组元素：通过 binarySearch 方法能对排序好的数组进行二分查找法操作。

| 序号 | 方法和说明                                                   |
| :--- | :----------------------------------------------------------- |
| 1    | **public static int binarySearch(Object[] a, Object key)** 用二分查找算法在给定数组中搜索给定值的对象(Byte,Int,double等)。数组在调用前必须排序好的。如果查找值包含在数组中，则返回搜索键的索引；否则返回 (-(*插入点*) - 1)。 |
| 2    | **public static boolean equals(long[] a, long[] a2)** 如果两个指定的 long 型数组彼此*相等*，则返回 true。如果两个数组包含相同数量的元素，并且两个数组中的所有相应元素对都是相等的，则认为这两个数组是相等的。换句话说，如果两个数组以相同顺序包含相同的元素，则两个数组是相等的。同样的方法适用于所有的其他基本数据类型（Byte，short，Int等）。 |
| 3    | **public static void fill(int[] a, int val)** 将指定的 int 值分配给指定 int 型数组指定范围中的每个元素。同样的方法适用于所有的其他基本数据类型（Byte，short，Int等）。 |
| 4    | **public static void sort(Object[] a)** 对指定对象数组根据其元素的自然顺序进行升序排列。同样的方法适用于所有的其他基本数据类型（Byte，short，Int等）。 |

# Date类

第一个构造函数使用当前日期和时间来初始化对象。

```java
Date( )
```

第二个构造函数接收一个参数，该参数是从1970年1月1日起的毫秒数。

```java
Date(long millisec)
```

Date对象创建以后，可以调用下面的方法。

| 序号 | 方法和描述                                                   |
| :--- | :----------------------------------------------------------- |
| 1    | **boolean after(Date date)** 若当调用此方法的Date对象在指定日期之后返回true,否则返回false。 |
| 2    | **boolean before(Date date)** 若当调用此方法的Date对象在指定日期之前返回true,否则返回false。 |
| 3    | **Object clone( )** 返回此对象的副本。                       |
| 4    | **int compareTo(Date date)** 比较当调用此方法的Date对象和指定日期。两者相等时候返回0。调用对象在指定日期之前则返回负数。调用对象在指定日期之后则返回正数。 |
| 5    | **int compareTo(Object obj)** 若obj是Date类型则操作等同于compareTo(Date) 。否则它抛出ClassCastException。 |
| 6    | **boolean equals(Object date)** 当调用此方法的Date对象和指定日期相等时候返回true,否则返回false。 |
| 7    | **long getTime( )** 返回自 1970 年 1 月 1 日 00:00:00 GMT 以来此 Date 对象表示的毫秒数。 |
| 8    | **int hashCode( )**  返回此对象的哈希码值。                  |
| 9    | **void setTime(long time)**   用自1970年1月1日00:00:00 GMT以后time毫秒数设置时间和日期。 |
| 10   | **String toString( )** 转换Date对象为String表示形式，并返回该字符串。 |

日期比较方法：getTime()，equals()/before()/after()，compareTo()

## 使用SimpleDateFormat格式化日期

SimpleDateFormat是一个以语言环境敏感的方式来格式化和分析日期的类。SimpleDateFormat允许你选择任何用户自定义日期时间格式来运行。例如：

```java
import java.util.*;
import java.text.*;

public class Main{
   public static void main(String args[]) {

      Date dNow = new Date( );
      SimpleDateFormat ft = 
      new SimpleDateFormat ("E yyyy.MM.dd 'at' hh:mm:ss a zzz");

      System.out.println("Current Date: " + ft.format(dNow));
   }
}
```

尝试一下

以上实例编译运行结果如下:

```java
Current Date: Sun 2004.07.18 at 04:14:09 PM PDT
```

## 简单的DateFormat格式化编码

时间模式字符串用来指定时间格式。在此模式中，所有的ASCII字母被保留为模式字母，定义如下：

| **字母** | **描述**                 | **示例**                |
| :------- | :----------------------- | :---------------------- |
| G        | 纪元标记                 | AD                      |
| y        | 四位年份                 | 2001                    |
| M        | 月份                     | July or 07              |
| d        | 一个月的日期             | 10                      |
| h        | A.M./P.M. (1~12)格式小时 | 12                      |
| H        | 一天中的小时 (0~23)      | 22                      |
| m        | 分钟数                   | 30                      |
| s        | 秒数                     | 55                      |
| S        | 毫秒数                   | 234                     |
| E        | 星期几                   | Tuesday                 |
| D        | 一年中的日子             | 360                     |
| F        | 一个月中第几周的周几     | 2 (second Wed. in July) |
| w        | 一年中第几周             | 40                      |
| W        | 一个月中第几周           | 1                       |
| a        | A.M./P.M. 标记           | PM                      |
| k        | 一天中的小时(1~24)       | 24                      |
| K        | A.M./P.M. (0~11)格式小时 | 10                      |
| z        | 时区                     | Eastern Standard Time   |
| '        | 文字定界符               | Delimiter               |
| "        | 单引号                   | `                       |

## 使用printf格式化日期

printf方法可以很轻松地格式化时间和日期。使用两个字母格式，它以t开头并且以下面表格中的一个字母结尾。例如：

```java
import java.util.Date;

public class Main{

  public static void main(String args[]) {
     // 初始化 Date 对象
     Date date = new Date();

     // 使用toString()显示日期和时间
     String str = String.format("Current Date/Time : %tc", date );

     System.out.printf(str);
  }
}
```

以上实例编译运行结果如下:

```java
Current Date/Time : Sat Dec 15 16:37:57 MST 2012
```

如果你需要重复提供日期，那么利用这种方式来格式化它的每一部分就有点复杂了。因此，可以利用一个格式化字符串指出要被格式化的参数的索引。

索引必须紧跟在%后面，而且必须以$结束。例如：

```java
import java.util.Date;
  
public class Main{
   public static void main(String args[]) {
       // 初始化 Date 对象
       Date date = new Date();
        
       // 使用toString()显示日期和时间
       System.out.printf("%1$s %2$tB %2$td, %2$tY", 
                         "Due date:", date);
   }
}
```

以上实例编译运行结果如下:

```java
Due date: February 09, 2004
```

或者，你可以使用<标志。它表明先前被格式化的参数要被再次使用。例如：

```java
import java.util.Date;
  
public class Main{

   public static void main(String args[]) {
       // 初始化 Date 对象
       Date date = new Date();
        
       // 显示格式化时间
       System.out.printf("%s %tB %<te, %<tY",
                           "Due date:", date);
   }
} 
```

以上实例编译运行结果如下:

```java
Due date: February 09, 2004
```

## 日期和时间转换字符

| **字符** | **描述**                         | **例子**                     |
| -------- | -------------------------------- | ---------------------------- |
| c        | 完整的日期和时间                 | Mon May 04 09:51:52 CDT 2009 |
| F        | ISO 8601 格式日期                | 2004-02-09                   |
| D        | U.S. 格式日期 (月/日/年)         | 02/09/2004                   |
| T        | 24小时时间                       | 18:05:19                     |
| r        | 12小时时间                       | 06:05:19 pm                  |
| R        | 24小时时间，不包含秒             | 18:05                        |
| Y        | 4位年份(包含前导0)               | 2004                         |
| y        | 年份后2位(包含前导0)             | 04                           |
| C        | 年份前2位(包含前导0)             | 20                           |
| B        | 月份全称                         | February                     |
| b        | 月份简称                         | Feb                          |
| n        | 2位月份(包含前导0)               | 02                           |
| d        | 2位日子(包含前导0)               | 03                           |
| e        | 2位日子(不包含前导0)             | 9                            |
| A        | 星期全称                         | Monday                       |
| a        | 星期简称                         | Mon                          |
| j        | 3位年份(包含前导0)               | 069                          |
| H        | 2位小时(包含前导0), 00 到 23     | 18                           |
| k        | 2位小时(不包含前导0),  0 到 23   | 18                           |
| I        | 2位小时(包含前导0), 01 到 12     | 06                           |
| l        | 2位小时(不包含前导0),  1 到 12   | 6                            |
| M        | 2位分钟(包含前导0)               | 05                           |
| S        | 2位秒数(包含前导0)               | 19                           |
| L        | 3位毫秒(包含前导0)               | 047                          |
| N        | 9位纳秒(包含前导0)               | 047000000                    |
| P        | 大写上下午标志                   | PM                           |
| p        | 小写上下午标志                   | pm                           |
| z        | 从GMT的RFC 822数字偏移           | -0800                        |
| Z        | 时区                             | PST                          |
| s        | 自 1970-01-01 00:00:00 GMT的秒数 | 1078884319                   |
| Q        | 自 1970-01-01 00:00:00 GMT的毫妙 | 1078884319047                |

还有其他有用的日期和时间相关的类。对于更多的细节，你可以参考到Java标准文档。

## Java 休眠(sleep)

你可以让程序休眠一==毫秒==的时间或者到您的计算机的寿命长的任意段时间。例如，下面的程序会休眠3秒：

```java
import java.util.*;
  
public class Main{
   public static void main(String args[]) {
      try { 
         System.out.println(new Date( ) + "\n"); 
         Thread.sleep(5*60*10); 
         System.out.println(new Date( ) + "\n"); 
      } catch (Exception e) { 
          System.out.println("Got an exception!"); 
      }
   }
}
```

以上实例编译运行结果如下:

```java
Sun May 03 18:04:41 GMT 2009

Sun May 03 18:04:44 GMT 2009
    
Difference is : 3050
```

# Calendar类

设置和获取日期数据的特定部分，比如说小时，日，或者分钟? 在日期的这些部分加上或者减去值呢? 

Calendar类是一个抽象类，在实际使用时实现特定的子类的对象，创建对象的过程对程序员来说是透明的，只需要使用getInstance方法创建即可。

## 创建一个指定日期的Calendar对象

使用Calendar类代表特定的时间，需要首先创建一个Calendar的对象，然后再设定该对象中的年月日参数来完成。

```java
//创建一个代表2009年6月12日的Calendar对象
Calendar c1 = Calendar.getInstance();
c1.set(2009, 6 - 1, 12);
```

## Calendar类对象字段类型

Calendar类中用一下这些常量表示不同的意义，jdk内的很多类其实都是采用的这种思想

| 常量                  | 描述                           |
| :-------------------- | :----------------------------- |
| Calendar.YEAR         | 年份                           |
| Calendar.MONTH        | 月份                           |
| Calendar.DATE         | 日期                           |
| Calendar.DAY_OF_MONTH | 日期，和上面的字段意义完全相同 |
| Calendar.HOUR         | 12小时制的小时                 |
| Calendar.HOUR_OF_DAY  | 24小时制的小时                 |
| Calendar.MINUTE       | 分钟                           |
| Calendar.SECOND       | 秒                             |
| Calendar.DAY_OF_WEEK  | 星期几                         |

## Calendar类对象信息的设置

**Set设置**

如：

```java
Calendar c1 = Calendar.getInstance();
```

调用：

```java
public final void set(int year,int month,int date)
c1.set(2009, 6 - 1, 12);//把Calendar对象c1的年月日分别设这为：2009、5、12
```

利用字段类型设置

如果只设定某个字段，例如日期的值，则可以使用如下set方法：

```java
public void set(int field,int value)
```

把 c1对象代表的日期设置为10号，其它所有的数值会被重新计算

```java
c1.set(Calendar.DATE,10);
```

把c1对象代表的年份设置为2008年，其他的所有数值会被重新计算

```java
c1.set(Calendar.YEAR,2008);
```

其他字段属性set的意义以此类推

**Add设置**

```java
Calendar c1 = Calendar.getInstance();
```

把c1对象的日期加上10，也就是c1所表的日期的10天后的日期，其它所有的数值会被重新计算

```java
c1.add(Calendar.DATE, 10);
```

把c1对象的日期减去10，也就是c1所表的日期的10天前的日期，其它所有的数值会被重新计算

```java
c1.add(Calendar.DATE, -10);
```

其他字段属性的add的意义以此类推

## Calendar类对象信息的获得

```java
Calendar c1 = Calendar.getInstance();
// 获得年份
int year = c1.get(Calendar.YEAR);
// 获得月份
int month = c1.get(Calendar.MONTH);
// 获得日期
int date = c1.get(Calendar.DATE);
// 获得小时
int hour = c1.get(Calendar.HOUR_OF_DAY);
// 获得分钟
int minute = c1.get(Calendar.MINUTE);
// 获得秒
int second = c1.get(Calendar.SECOND);
// 获得星期几（注意（这个与Date类是不同的）：1代表星期日、2代表星期1、3代表星期二，以此类推）
int day = c1.get(Calendar.DAY_OF_WEEK);
```

# GregorianCalendar类

Calendar类实现了公历日历，GregorianCalendar是Calendar类的一个具体实现。

Calendar 的getInstance（）方法返回一个默认用当前的语言环境和时区初始化的GregorianCalendar对象。GregorianCalendar定义了两个字段：AD和BC。这些代表公历定义的两个时代。

下面列出GregorianCalendar对象的几个构造方法：

| **序号** | **构造函数和说明**                                           |
| -------- | ------------------------------------------------------------ |
| 1        | **GregorianCalendar()** 在具有默认语言环境的默认时区内使用当前时间构造一个默认的 GregorianCalendar。 |
| 2        | **GregorianCalendar(int year, int month, int date)** 在具有默认语言环境的默认时区内构造一个带有给定日期设置的 GregorianCalendar |
| 3        | **GregorianCalendar(int year, int month, int date, int hour, int minute)** 为具有默认语言环境的默认时区构造一个具有给定日期和时间设置的 GregorianCalendar。 |
| 4        | **GregorianCalendar(int year, int month, int date, int hour, int minute, int second)**  为具有默认语言环境的默认时区构造一个具有给定日期和时间设置的 GregorianCalendar。 |
| 5        | **GregorianCalendar(Locale aLocale)** 在具有给定语言环境的默认时区内构造一个基于当前时间的 GregorianCalendar。 |
| 6        | **GregorianCalendar(TimeZone zone)** 在具有默认语言环境的给定时区内构造一个基于当前时间的 GregorianCalendar。 |
| 7        | **GregorianCalendar(TimeZone zone, Locale aLocale)**  在具有给定语言环境的给定时区内构造一个基于当前时间的 GregorianCalendar。 |

这里是GregorianCalendar 类提供的一些有用的方法列表：

| **序号** | **方法和说明**                                               |
| -------- | ------------------------------------------------------------ |
| 1        | **void add(int field, int amount)** 根据日历规则，将指定的（有符号的）时间量添加到给定的日历字段中。 |
| 2        | **protected void computeFields()** 转换UTC毫秒值为时间域值   |
| 3        | **protected void computeTime()** 覆盖Calendar ，转换时间域值为UTC毫秒值 |
| 4        | **boolean equals(Object obj)** 比较此 GregorianCalendar 与指定的 Object。 |
| 5        | **int get(int field)** 获取指定字段的时间值                  |
| 6        | **int getActualMaximum(int field)** 返回当前日期，给定字段的最大值 |
| 7        | **int getActualMinimum(int field)** 返回当前日期，给定字段的最小值 |
| 8        | **int getGreatestMinimum(int field)**  返回此 GregorianCalendar 实例给定日历字段的最高的最小值。 |
| 9        | **Date getGregorianChange()** 获得格里高利历的更改日期。     |
| 10       | **int getLeastMaximum(int field)** 返回此 GregorianCalendar 实例给定日历字段的最低的最大值 |
| 11       | **int getMaximum(int field)** 返回此 GregorianCalendar 实例的给定日历字段的最大值。 |
| 12       | **Date getTime()** 获取日历当前时间。                        |
| 13       | **long getTimeInMillis()** 获取用长整型表示的日历的当前时间  |
| 14       | **TimeZone getTimeZone()** 获取时区。                        |
| 15       | **int getMinimum(int field)** 返回给定字段的最小值。         |
| 16       | **int hashCode()** 重写hashCode.                             |
| 17       | **boolean isLeapYear(int year)** 确定给定的年份是否为闰年。  |
| 18       | **void roll(int field, boolean up)** 在给定的时间字段上添加或减去（上/下）单个时间单元，不更改更大的字段。 |
| 19       | **void set(int field, int value)** 用给定的值设置时间字段。  |
| 20       | **void set(int year, int month, int date)** 设置年、月、日的值。 |
| 21       | **void set(int year, int month, int date, int hour, int minute)** 设置年、月、日、小时、分钟的值。 |
| 22       | **void set(int year, int month, int date, int hour, int minute, int second)** 设置年、月、日、小时、分钟、秒的值。 |
| 23       | **void setGregorianChange(Date date)** 设置 GregorianCalendar 的更改日期。 |
| 24       | **void setTime(Date date)** 用给定的日期设置Calendar的当前时间。 |
| 25       | **void setTimeInMillis(long millis)** 用给定的long型毫秒数设置Calendar的当前时间。 |
| 26       | **void setTimeZone(TimeZone value)** 用给定时区值设置当前时区。 |
| 27       | **String toString()** 返回代表日历的字符串。                 |

## 实例

```java
import java.util.*;
  
public class GregorianCalendarDemo {

   public static void main(String args[]) {
      String months[] = {
      "Jan", "Feb", "Mar", "Apr",
      "May", "Jun", "Jul", "Aug",
      "Sep", "Oct", "Nov", "Dec"};
      
      int year;
      // 初始化 Gregorian 日历
      // 使用当前时间和日期
      // 默认为本地时间和时区
      GregorianCalendar gcalendar = new GregorianCalendar();
      // 显示当前时间和日期的信息
      System.out.print("Date: ");
      System.out.print(months[gcalendar.get(Calendar.MONTH)]);
      System.out.print(" " + gcalendar.get(Calendar.DATE) + " ");
      System.out.println(year = gcalendar.get(Calendar.YEAR));
      System.out.print("Time: ");
      System.out.print(gcalendar.get(Calendar.HOUR) + ":");
      System.out.print(gcalendar.get(Calendar.MINUTE) + ":");
      System.out.println(gcalendar.get(Calendar.SECOND));
      
      // 测试当前年份是否为闰年
      if(gcalendar.isLeapYear(year)) {
         System.out.println("当前年份是闰年");
      }
      else {
         System.out.println("当前年份不是闰年");
      }
   }
}
```

以上实例编译运行结果如下：

```java
Date: Apr 22 2009
Time: 11:25:27
当前年份不是闰年
```

关于Calender 类的完整列表，你可以参考标准的Java文档。

# [回到首页](./index.html)

