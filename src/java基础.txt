# 基本数据类型

## 整型

### byte

8位，有符号，二进制补码表示，-127~128，默认为0

### short

16位，有符号，二进制补码表示，-32678~32677，默认为0

### int

32位，-2147483648~2147483647

### long

64位，默认0L

## 浮点型

### float

单精度，32位，默认0.0f

### double

双精度，64位，默认0.0d

## 布尔型

### boolean

true或false，默认为false

## 字符型

### char

16位Unicode字符，最小值`\u0000`(0)，最大值`\uffff`(65535)。可以存储任何字符

## 取值范围

```c++
public class PrimitiveTypeTest {
    public static void main(String[] args) {
    // byte
    System.out.println("基本类型：byte 二进制位数：" + Byte.SIZE);
    System.out.println("包装类：java.lang.Byte");
    System.out.println("最小值：Byte.MIN_VALUE=" + Byte.MIN_VALUE);
    System.out.println("最大值：Byte.MAX_VALUE=" + Byte.MAX_VALUE);
    System.out.println();
    
    // short
    System.out.println("基本类型：short 二进制位数：" + Short.SIZE);
    System.out.println("包装类：java.lang.Short");
    System.out.println("最小值：Short.MIN_VALUE=" + Short.MIN_VALUE);
    System.out.println("最大值：Short.MAX_VALUE=" + Short.MAX_VALUE);
    System.out.println();

    // int
    System.out.println("基本类型：int 二进制位数：" + Integer.SIZE);
    System.out.println("包装类：java.lang.Integer");
    System.out.println("最小值：Integer.MIN_VALUE=" + Integer.MIN_VALUE);
    System.out.println("最大值：Integer.MAX_VALUE=" + Integer.MAX_VALUE);
    System.out.println();

    // long
    System.out.println("基本类型：long 二进制位数：" + Long.SIZE);
    System.out.println("包装类：java.lang.Long");
    System.out.println("最小值：Long.MIN_VALUE=" + Long.MIN_VALUE);
    System.out.println("最大值：Long.MAX_VALUE=" + Long.MAX_VALUE);
    System.out.println();

    // float
    System.out.println("基本类型：float 二进制位数：" + Float.SIZE);
    System.out.println("包装类：java.lang.Float");
    System.out.println("最小值：Float.MIN_VALUE=" + Float.MIN_VALUE);
    System.out.println("最大值：Float.MAX_VALUE=" + Float.MAX_VALUE);
    System.out.println();

    // double
    System.out.println("基本类型：double 二进制位数：" + Double.SIZE);
    System.out.println("包装类：java.lang.Double");
    System.out.println("最小值：Double.MIN_VALUE=" + Double.MIN_VALUE);
    System.out.println("最大值：Double.MAX_VALUE=" + Double.MAX_VALUE);
    System.out.println();

    // char
    System.out.println("基本类型：char 二进制位数：" + Character.SIZE);
    System.out.println("包装类：java.lang.Character");
    // 以数值形式而不是字符形式将Character.MIN_VALUE输出到控制台
    System.out.println("最小值：Character.MIN_VALUE="
            + (int) Character.MIN_VALUE);
    // 以数值形式而不是字符形式将Character.MAX_VALUE输出到控制台
    System.out.println("最大值：Character.MAX_VALUE="
            + (int) Character.MAX_VALUE);
}
} 
```

## 引用类型

引用类型变量由类的构造函数创建，**类型不可变**。

对象、数组是引用类型

默认为null

可以引用与之兼容的任何类型

## Java常量

用final标志变量为常量

前缀0表示8进制数，前缀0x代表16进制

字符串常量和字符常量可以包含任何Unicode字符

`String s = "\u0a78";`

特殊的转义字符

|符号     |字符含义                  |
| ------ | ------------------------ |
| \n     | 换行 (0x0a)              |
| \r     | 回车 (0x0d)              |
| \f     | 换页符(0x0c)             |
| \b     | 退格 (0x08)              |
| \0     | 空字符（0x0）            |
| \s     | 字符串                   |
| \t     | 制表符                   |
| \"     | 双引号                   |
| \'     | 单引号                   |
| \\     | 反斜杠                   |
| \ddd   | 八进制字符 (ddd)         |
| \uxxxx | 16进制Unicode字符 (xxxx) |

# 变量类型

## 局部变量

`age`是一个局部变量，定义在`pupAge()`方法中，其作用域限制在这个方法中。

```java
public class Test{ 
   public void pupAge(){
      int age = 0;
      age = age + 7;
      System.out.println("Puppy age is : " + age);
   }
   
   public static void main(String args[]){
      Test test = new Test();
      test.pupAge();
   }
}
```

## 实例变量

类中，构造方法，方法，语句块之外

跟着实例化的对象

其值至少被一个方法，构造方法或语句块引用，使外部能通过这些方式获取实例变量信息

==实例变量可以声明在使用前或使用后==

访问修饰符修饰实例变量

实例变量对于类中的方法，构造方法和语句块是可见的。一般情况下应把实例变量设为私有（private）。可以通过访问修饰符使实例变量对子类可见（public）

默认值。数值型为0，布尔型为false，引用型为null。变量值可以在声明时指定，也可以在构造方法中指定。

可直接通过变量名访问。但在**静态方法**和其他类中，就应该使用完全限定名：`ObejectReference.VariableName`。

```java
import java.io.*;
public class Employee{
   // 这个成员变量对子类可见
   public String name;
   // 私有变量，仅在该类可见
   private double salary;
   //在构造器中对name赋值
   public Employee (String empName){
      name = empName;
   }
   //设定salary的值
   public void setSalary(double empSal){
      salary = empSal;
   }  
   // 打印信息
   public void printEmp(){
      System.out.println("name  : " + name );
      System.out.println("salary :" + salary);
   }

   public static void main(String args[]){
      Employee empOne = new Employee("Ransika");
      empOne.setSalary(1000);
      empOne.printEmp();
   }
}
```

## 类变量（静态变量）

在类中以static关键字声明，必须在方法，构造方法，语句块之外

无论创建多少对象，类只有类变量的一份拷贝

一般被声明为常量

拥有程序生命周期

默认值与实例变量相似

可以通过`ClassName.VariableName`的方式访问

如果被声明为public static final，一般采用大写字母

```java
import java.io.*;
public class Employee{
   //salary是静态的私有变量
   private static double salary;
   // DEPARTMENT是一个常量
   public static final String DEPARTMENT = "Development ";
   public static void main(String args[]){
      salary = 1000;
      System.out.println(DEPARTMENT+"average salary:"+salary);
   }
}
```

# 修饰符

## 访问修饰符

默认的，也称为 default，在**同一包**内可见，不使用任何修饰符。

私有的，以 private 修饰符指定，在**同一类**内可见。

公有的，以 public 修饰符指定，对**所有类**可见。

受保护的，以 protected 修饰符指定，对**同一包内的类和所有子类**可见。

### 默认访问修饰符

默认访问修饰符声明的变量对同一个包中的类都是可见的。

接口里的变量都隐式声明为`public static final`

接口里的方法默认情况下访问权限为`public`

### 私有访问修饰符

被声明为`private`的变量，构造方法，方法只能被所属类访问，并且类和接口不能声明为`private`

声明为私有访问类型的变量只能被类中公共的getter方法被外部类访问

private修饰符主要用来隐藏类的实现细节和保护类的数据

```java
public class Logger {
   private String format;
   public String getFormat() {
      return this.format;
   }
   public void setFormat(String format) {
      this.format = format;
   }
}
```

Logger类中的format变量被声明为private，其他类不能得到和设置这个变量的值。为了使其他类能操作该变量，定义两个public方法：getFormat（得到format的值）和setFormat（设置format的值）

### 公共访问修饰符

被声明为public的类，方法，构造方法，接口可以被任何其他类访问

如果有几个相互访问的类分布在不同的包中，则需要导入相应public所在的包。由于类的继承性，类所有的公有属性和方法都能被其子类继承。

### 受保护的访问修饰符

能被同一个包中的任何其他类访问，也可以被其他包中的子类访问。

不能修饰类和接口，只能修饰成员变量和方法，但是接口的成员变量和方法不能声明为protected

子类能访问protected修饰声明的方法和变量，保护不相关的类使用这些变量和方法

```java
class AudioPlayer {
   protected boolean openSpeaker(Speaker sp) {
      // 实现细节
   }
}

class StreamingAudioPlayer extends AudioPlayer {
   boolean openSpeaker(Speaker sp) {
      // 实现细节
   }
}
```

如果将openSpeaker声明为private，那么除AudioPlayer的类将不能访问此方法

如果将openSpeaker声明为public，那么所有类都可以访问此方法

如果将openSpeaker声明为protected，那么其对AudioPlayer的子类可见

### 访问控制与继承

- 父类中声明为 public 的方法在子类中也必须为 public。
- 父类中声明为 protected 的方法在子类中要么声明为 protected，要么声明为 public。不能声明为 private。
- 父类中声明为 private 的方法，不能够被继承。

## 非访问修饰符

### static修饰符

#### 静态变量

#### 静态方法

对类变量和方法的访问可以直接使用 `classname.variablename` 和 `classname.methodname` 的方式访问。

```java
public class InstanceCounter {
   private static int numInstances = 0;
   protected static int getCount() {
      return numInstances;
   }

   private static void addInstance() {
      numInstances++;
   }

   InstanceCounter() {
      InstanceCounter.addInstance();
   }

   public static void main(String[] arguments) {
      System.out.println("Starting with " +
      InstanceCounter.getCount() + " instances");
      for (int i = 0; i < 500; ++i){
          new InstanceCounter();
      }
      System.out.println("Created " +
       InstanceCounter.getCount() + " instances");
   }
} 
```

### final修饰符

#### final变量

final对象的引用不能变，但final对象的引用的对象可以变。

```java
public class Test{
  final int value = 10;
  // 下面是声明常量的实例
  public static final int BOXWIDTH = 6;
  static final String TITLE = "Manager";

  public void changeValue(){
     value = 12; //将输出一个错误
  }
}
```

#### final方法

可以被子类继承，但不能被子类修改。

#### final类

不能被继承

### 抽象类

抽象类不能用来实例化对象，声明抽象类的唯一目的是为了**将来对该类进行扩充**。

一个类**不能同时被 abstract 和 final 修饰**。如果一个类包含抽象方法，那么该类一定要声明为抽象类，否则将出现编译错误。

抽象类可以包含抽象方法和非抽象方法。

实例：

```java
abstract class Caravan{
   private double price;
   private String model;
   private String year;
   public abstract void goFast(); //抽象方法
   public abstract void changeColor();
}
```

### 抽象方法

抽象方法是一种没有任何实现的方法，该方法的的具体实现由子类提供。抽象方法不能被声明成 final 和 static。

任何**继承抽象类的子类**必须实现父类的**所有**抽象方法，**除非**该子类也是抽象类。

如果一个类包含若干个抽象方法，那么该类**必须**声明为抽象类。抽象类**可以不包含**抽象方法。

抽象方法的声明以分号结尾，例如：public abstract sample();

实例：

```java
public abstract class SuperClass{
    abstract void m(); //抽象方法
}
 
class SubClass extends SuperClass{
     //实现抽象方法
      void m(){
          .........
      }
}
```

### synchronized 修饰符

synchronized 关键字声明的方法同一时间只能被一个线程访问。Synchronized 修饰符可以应用于==四个访问修饰符==。

实例：

```java
public synchronized void showDetails(){
.......
} 
```

### transient 修饰符

序列化的对象包含被 transient 修饰的实例变量时，java 虚拟机 (JVM) 跳过该特定的变量。

该修饰符包含在定义变量的语句中，用来==**预处理类和变量的数据类型**==。

实例：

```java
public transient int limit = 55;   // will not persist
public int b; // will persist
```

### volatile修饰符

volatile 修饰的成员变量在每次被线程访问时，都强迫从共享内存中重读该成员变量的值。而且，当成员变量发生变化时，强迫线程将变化值回写到共享内存。这样在任何时刻，==两个不同的线程总是看到某个成员变量的同一个值==。

一个 volatile 对象引用可能是 null。

实例：

```java
public class MyRunnable implements Runnable
{
    private volatile boolean active;
    public void run()
    {
        active = true;
        while (active) // line 1
        {
            // 代码
        }
    }
    public void stop()
    {
        active = false; // line 2
    }
}
```

一般地，在一个线程中调用run()方法，在另一个线程中调用stop()方法。如果line 1中的active位于缓冲区的值被使用，那么当把line 2中的active设置成false时，循环也不会停止。

# Instanceof运算符

操作对象实例，检查该对象是否是一个特定类型（类类型或接口类型）

使用格式如下：

```java
( Object reference variable ) instanceof  (class/interface type)
```

```java
String name = 'James';
boolean result = name instanceof String;
```

例子：

```java
class Vehicle {}

public class Car extends Vehicle {
   public static void main(String args[]){
      Vehicle a = new Car();
      boolean result =  a instanceof Car;
      System.out.println( result);
   }
}
```

以上实例编译运行结果如下：

```java
true
```

# 增强for循环

Java5引入

Java增强for循环语法格式如下:

```java
for(声明语句 : 表达式)
{
   //代码句子
}
```

**声明语句：**声明新的局部变量，该变量的类型必须和数组元素的类型匹配。其作用域限定在循环语句块，其值与此时数组元素的值相等。

**表达式：**表达式是要访问的数组名，或者是返回值为数组的方法。

```java
public class Test {

   public static void main(String args[]){
      int [] numbers = {10, 20, 30, 40, 50};

      for(int x : numbers ){
         System.out.print( x );
         System.out.print(",");
      }
      System.out.print("\n");
      String [] names ={"James", "Larry", "Tom", "Lacy"};
      for( String name : names ) {
         System.out.print( name );
         System.out.print(",");
      }
   }
}
```

以上实例编译运行结果如下：

```java
10,20,30,40,50,
James,Larry,Tom,Lacy,
```

# [回到首页](./index.html)
