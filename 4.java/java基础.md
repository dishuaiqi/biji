# java基础



## 2.1环境搭建

![image-20230118151011557](D:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20230118151011557.png)

下载java1.8  https://www.oracle.com/cn/java/technologies/downloads/#java8

加入环境变量

下载编译器（IDE)

![image-20230118155356593](D:\Users\Administrator\AppData\Roaming\Typora\typora-user-images\image-20230118155356593.png)

https://www.jetbrains.com/idea/download/other.html

## 2.3 JAVA基础语法

初步代码的分析：Hello.java

```java
public class hello {
    public static void main(String[] args) {
        System.out.println("哈哈哈");
    }
}
```

- 主函数&程序的入口

  ```python
  def func():
      pass
  if __name__ =="main":
      func()
  ```

- 文件名

  ```
  一个文件最多只能有一个public类 且文件名必须和public类名一致。
  如果文件中有多个类，文件名与public类名一致。
  如果文件中有多个类，且无public类，文件名可以是任意类名。
  ```

- 类名

  ```
  首字母大写，且驼峰式命名，例如Hello,UserInfo,PersonApplication
  ```

- 类修饰符:public（表示公有的，在任何地方都可以调用这个类）、default(不写)

- 类成员修饰符：成员是指类里面的成员。 有public、private、protected、default(不写)

- 静态成员，无序实例化就可以指定调用。

  ```java
  class MyTest{
      public void f1(){
          System.out.println("f1");
      }
      public static void f2(){               //静态
          System.out.println("f2");
      }
  }
  
  
  public class hello {
      public static void main(String[] args) {
          //1.实例化
          MyTest obj=new MyTest();
          //2.对象调用
          obj.f1();
  
          MyTest.f2();
      }
  }
  ```

  ​	pytho中也是如此

  ```python
  class Foo:
  #     绑定方法
      def f1(self):
          print('f1')
      # 静态方法
      @staticmethod
      def f2():
          print('f2')
  # 调用f1
  obj=Foo()
  obj.f1()
  
  # 调用f2
  Foo.f2()
  
  ```

  