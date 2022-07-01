# 基础

## 代码结构

![img](java.assets/7D`MG0H3%FDNZ`NM{3[9{8.png)

###  包机制



![image-20220615112240049](java.assets/image-20220615112240049.png)





## 注释

多行注释 : 注释一段文字   /*   */

单行注释:    // 



### 文档注释: 

```
/**   
*@Description 
*@
*/
```

![](java.assets/image-20220615113644997.png)

命令行

```cmd
javadoc -encoding UTF-8 -charset UTF-8 文件名
```





## 标识符

![image-20220615092413691](java.assets/image-20220615092413691.png)



## 数据类型

![image-20220615092719547](java.assets/image-20220615092719547.png)

### 基本数据类型

==**有默认值**==

![image-20220615092903118](java.assets/image-20220615092903118.png)



### 整数扩展

![image-20220615094501808](java.assets/image-20220615094501808.png)

### 浮点数扩展

![image-20220615094538891](java.assets/image-20220615094538891.png)

### 字符扩展

![image-20220615094606854](java.assets/image-20220615094606854.png)





## 类型转换

![image-20220615095235290](java.assets/image-20220615095235290.png)

### 重要

![image-20220615095330221](java.assets/image-20220615095330221.png)



![image-20220615100009692](java.assets/image-20220615100009692.png)







```java
public class hello {
    //输出
    public static void main(String[] args){
        System.out.println("=================");
        char c = 'a';
        int d = c+1;
        System.out.println(d);  // 显示转换   98
        System.out.println((char)d);  // 高到低  隐式转换  b
    }
}
```



### 已经出现问题

![image-20220615100130953](java.assets/image-20220615100130953.png)







## 变量

![image-20220615101818865](java.assets/image-20220615101818865.png)

### 要求

+ **只有常量是全大写有下划线**
+ **其他全部遵守驼峰原则**
+ **类是首字母大写再遵守驼峰原则**

![](java.assets/image-20220615105430302.png)



### 变量作用域

![image-20220615103528029](java.assets/image-20220615103528029.png)

![image-20220615103621637](java.assets/image-20220615103621637.png)



###  核心

```java
public class variable {

    // 类变量: static
    static double salary = 2000;

    //属性：变量

    //实例变量：从属于对象；如果不自行初始化，这个类型的默认值 0 0.0
    //布尔值：默认是false
    //除了基本类型，其余的默认值都是null；
    String name;
    int age;

    //main方法
    public static void main(String[] args) {

        //局部变量；
        //必须声明和初始化值
        int i = 10;
        System.out.println(i);;

        //实例变量:
        // 变量类型 变量名字 = new variable()；
        variable var = new variable();
        System.out.println(var.age);
        System.out.println(var.name);

        //类变量 static
        System.out.println(salary);
    }

}
```





## 常量

修饰符  final

```java
final double pi = 3.14;
```

final之后是不能被继承的

## 运算符

![](java.assets/image-20220615110226079.png)



### ** 字符串连接符 + **

```c++
// 字符串连接符 + , String
int a = 10;
int b = 30;
System.out.println("" + a + b);   // 会进行拼接
System.out.println(a + b + "");   // 不会进行拼接
```





### 三元运算符

**m  =  x < y ? x : y**







##  输入

## 使用方法

![image-20220618080918483](java.assets/image-20220618080918483.png)



![image-20220618080929207](java.assets/image-20220618080929207.png)

##  单个输入

![image-20220618081114645](java.assets/image-20220618081114645.png)

## 整行输入

![image-20220618081139777](java.assets/image-20220618081139777.png)

## 读取整数,小数

![image-20220618082132166](java.assets/image-20220618082132166.png)



```c++
package com.jindao;

import java.util.Scanner;

public class Scan {
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);
        double sum = 0;
        int count = 0;
        System.out.println("请输入数字(输入不是数字退出)");
        while (scanner.hasNextDouble())
        {
            double x = scanner.nextDouble();
            count++;
            sum+= x;
        }
        System.out.println(count + "个数的和为" + sum);
        System.out.println(count + "个数的平均值" + sum/count);
    }
}
```





##  顺序结构

![image-20220618082951963](java.assets/image-20220618082951963.png)

选择结构



![image-20220618083058214](java.assets/image-20220618083421117.png)



![image-20220618083636991](java.assets/image-20220618083636991.png) 

## 循环结构



![image-20220618084818276](java.assets/image-20220618084818276.png)







![img](java.assets/QG`T06XYKFQA{T_FYY5`GIQ.png)



## for循环

![image-20220618085558828](java.assets/image-20220618085558828.png)



**100.for直接生成**

**for (;;;)  --- > 死循环**





![image-20220618090840872](java.assets/image-20220618090840872.png)

###  99乘法表

```java
package com.jindao;

public class Fordemo02 {
    public static void main(String[] args) {
        for (int i = 1; i <= 9; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print(i + "*" + j + "=" + i*j + "\t");
            }
            System.out.println();
        }
    }
}
```



## break和continue

![image-20220618092001474](java.assets/image-20220618092001474.png)



![image-20220618093053755](java.assets/image-20220618093053755.png)





## 方法



+ **修饰符 返回类型 方法名(参数)** 

### 方法的定义

![image-20220618093631237](java.assets/image-20220618093631237.png)

### 方法的调用

![img](java.assets/7[}({I8`)[W_UW}TU50$C32.png) 

####  静态方法

![image-20220619090714050](java.assets/image-20220619090714050.png)



#### 非静态方法

![image-20220619090846781](java.assets/image-20220619090846781.png)



#### 两者区别

![image-20220619090937803](java.assets/image-20220619090937803.png)







### 方法的重载

![image-20220618094455162](java.assets/image-20220618094455162.png)



## 命令行传参

![img](java.assets/3GT3Q%{J9LURANL_RDNCKHC.png)





## 可变参数

![img](java.assets/ZI}8S42W%924JH${Y7[Z2[F.png)



例子:

![](java.assets/QQ图片20220618095536.png)





递归



![递归](java.assets/QQ图片20220618100036.png)







## 数组



==**int[]    表示数组类型**==



![img](java.assets/JS{R}D2ZO]{IQJ_I$_WWBYH.png)



### 内存分析



![image-20220618101753948](java.assets/image-20220618101753948.png)



### 三种初始化方式



![](java.assets/QQ图片20220618102214.png)



![img](java.assets/5Z4{@4K4S%B@V@95F4BP{95.png)



![](java.assets/QQ图片20220618102235.png)



+ **动态初始化有默认的值   int 对应 0  **





**数组的基本特点**

![](java.assets/QQ图片20220618103116.png)



![](java.assets/QQ图片20220618103239.png)







###  数组使用



![img](java.assets/%}N@510G}RQH_YJVQ$NE9WT.png)





### 二维数组

![img](java.assets/6C6NZQ2K8J3E1AQT]O2_VJS.png)



![](java.assets/QQ图片20220618105028.png)

**图示:**

![img](java.assets/L_ZSOCCS5]2AYD]A%YVCY5V.png)

## Arrays类



![image-20220618110259411](java.assets/image-20220618110259411.png)





## 冒泡排序

![](java.assets/QQ图片20220618110415.png)



![![()](java.assets/QQ图片20220618110836.png)



###  代码

```java
package com.jindao;

import java.util.Arrays;

public class ArrayDemo03 {
    public static void main(String[] args) {
        int[] array = {1, 4, 5, 6, 72, 2, 2, 2, 25, 6, 7};
        int[] sort = sort(array);
        System.out.println(Arrays.toString(sort));
    }
    
    public static int[] sort(int[] array) { 
        for (int i = 0; i < array.length - 1; i++) {    // 交换的次数
            boolean flag = false;
            for (int j = 0; j < array.length-1-i; j++) {
                if (array[j+1] >= array[j]) {
                    array[j] ^= array[j+1];
                    array[j+1] ^= array[j];
                    array[j] ^= array[j+1];
                    flag = true;
                }
            }
        }
        if (flag = false)
            break;
        
        return array;
    }
}

```

----------------



## 稀疏数组



![img](java.assets/SB7}9A2ZG9S%[7MPVB@SA%6.png)







![img](java.assets/7O5H{0BFLZ%1N]RYT41J9GI.png)



![img](java.assets/7D]DTW%JJKCPW2B}7AJXB0.png)





```java
package com.jindao;

public class ArrayDemo04 {
    public static void main(String[] args) {
        int[][] array1 = new int[11][11];
        array1[1][2] = 1;
        array1[2][3] = 2;
        System.out.println("输出原始数组:");
        for (int[] ints : array1) {
            for(int n : ints) {
                System.out.print(n+"\t");
            }
            System.out.println();
        }

        // 稀疏数组
        //1.获取有效个数
        int sum = 0;
        for (int i = 0; i < 11; i++) {
            for (int i1 = 0; i1 < 11; i1++) {
                if (array1[i][i1] != 0)
                    sum++;
            }
        }
        System.out.println("有效个数: " + sum);

        //2.创建稀疏数组
        int[][] array2 = new int[sum + 1][3];
        // 初始化, 行列非零值数量
        array2[0][0] = 11;
        array2[0][1] = 11;
        array2[0][2] = sum;
        //存非零值
        int count = 0;
        for (int i = 0; i < array1.length; i++) {
            for (int i1 = 0; i1 < array1[i].length; i1++) {
                if (array1[i][i1] != 0) {
                    count++;
                    array2[count][0] = i;
                    array2[count][1] = i1;
                    array2[count][2] = array1[1][i1];
                }
            }
        }

        // 输出稀疏数组
        System.out.println("稀疏数组");
        for (int i = 0; i < array2.length; i++) {
            System.out.println(array2[i][0] + "\t"
                    + array2[i][1] + "\t"
                    + array2[i][2] + "\t");
        }

        // 还原稀疏数组
        //1.读取
        int[][] array3 = new int[array2[0][0]][array2[0][1]];
        //2.还原
        for (int i = 1; i < array2.length; i++) {
            array3[array2[i][0]][array2[i][1]] = array2[i][2];
        }
        //3.打印
        for (int[] ints : array3) {
            for(int n : ints) {
                System.out.print(n+"\t");
            }
            System.out.println();
        }
    }
}

```

![](java.assets/QQ图片20220619085001.png)



-----------------



# 面向对象

## 类与对象创建

![image-20220619092232782](java.assets/image-20220619092232782.png)





## 构造器



![image-20220619092916448](java.assets/image-20220619092916448.png)

快捷键

**alt+insert----->可以快捷生成**

![](java.assets/QQ图片20220619093124.png)



**this.属性 = 进行初始化**

-----------





## 创建对象内存分析



![](../../QQ图片20220619093750.png)

![](java.assets/QQ图片20220619093747.png)

-------------------------

## 小结



![image-20220619094315068](java.assets/image-20220619094315068.png)

![](java.assets/QQ图片20220619094332.png)



## 封装

![image-20220619094504210](java.assets/image-20220619094504210.png)

![img](java.assets/{LCGMF1(QC]PKQVTFC)DM_X.png)



## 继承



![img](java.assets/W_PZX`V86AQBHFSK3X9JT}0.png)



### super

![](java.assets/QQ图片20220619100710.png)





![](java.assets/QQ图片20220619101108.png)



###  方法的重写

![image-20220619104209632](java.assets/image-20220619104209632.png)

![](java.assets/QQ图片20220619103628.png)

![img](java.assets/LK%R{2DNADGNXVW_$9R{3$V.png)

**不能重写的**

![](java.assets/QQ图片20220619105502.png)



--------------



## 多态

#### 基础

![img](java.assets/ESZFFH@%P9{I8N$GLN$]R.png)



![image-20220619104723563](java.assets/image-20220619104723563.png)

![image-20220619104815539](java.assets/image-20220619104815539.png)



![](java.assets/image-20220619104857503.png)

![image-20220619105408006](java.assets/image-20220619105408006.png)



---------



### instanceof和类型转换



 x  instanof y      // 



![img](java.assets/DS7Q8`V88671K%YOYN0EQY7.png)



![img](java.assets/ZV58([Z6R(AH])5EL@EH99C.png)





## static

1. **静态代码块**

![img](java.assets/5DI6{NDFO65YX@K37P`_A]D.png)

![img](java.assets/THHTU`JB$ZAE2@5UNDCFQ.png)





2. **静态导入包**

![](java.assets/QQ图片20220620084350.png)



3. **静态方法**

![image-20220620084528131](java.assets/image-20220620084528131.png)





## 抽象类



![](java.assets/QQ图片20220620085512.png)







## 接口

**利用接口实现多继承**

![](java.assets/QQ图片20220620085634.png)





![](java.assets/QQ图片20220620091546.png)



![](java.assets/QQ图片20220620091718.png)



![](java.assets/QQ图片20220620091855.png)







## 内部类

### 1.正常的

![img](java.assets/P76M6DWOZ5Y3R$S7ECSSZYJ.png)

![](java.assets/QQ图片20220620093134.png)

### **2. 局部内部类**

![](java.assets/QQ图片20220620093407.png)



### 3. 没有名字的初始化类

**可以简单的使用方法**

![](java.assets/QQ图片20220620093703.png)



## 异常

### 基础

![img](java.assets/4O{BE94M8JJJ30YM%IM1Y7N.png)



![](java.assets/QQ图片20220620094243.png)

![](java.assets/QQ图片20220620094331.png)

![](java.assets/QQ图片20220620094433.png)



![](java.assets/QQ图片20220620094552.png)





###  捕获抛出异常

**代码块的捕获异常**

![img](java.assets/QQ图片20220620094833.png)



![](java.assets/QQ图片20220620095025.png)

自动填写代码

![](java.assets/QQ图片20220620095114.png)





**抛出方法的异常**

![](java.assets/QQ图片20220620095429.png)







###  自定义异常类



![image-20220620100439669](java.assets/image-20220620100439669.png)



**test ; **



![](java.assets/QQ图片20220620100352.png)



![](java.assets/QQ图片20220620100631.png)



