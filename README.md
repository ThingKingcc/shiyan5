### 陈玺庆 2019322056 计G191 
## 1、实验目的

分析学生选课系统
使用GUI窗体及其组件设计窗体界面

完成学生选课过程业务逻辑编程

基于文件保存并读取数据处理异常



## 2、实验要求

例如：学校有“人员”，分为“教师”和“学生”，教师教授“课程”，学生选择课程。

定义每种角色人员的属性，及其操作方法。

属性实例： 人员（编号、性别、姓名）
          教师（编号、姓名、性别、所授课程）
          学生（编号、姓名、性别、所选课程）
          课程（编号、课程名称、上课地点、时间、授课教师）
          

## 3、程序代码：


package Zuoye;

 import java.util.Scanner;

 public class Lianxi {
     public static void main(String args[]) {
         try {
             if (args.length == 0) {
                 throw new IllegalArgumentException("Please input 长恨歌");
             }
         } catch (IllegalArgumentException e) {
             System.err.println(e.getMessage());
         }
         String res = args[0];
         for(int i = 0; i < res.length(); i++){
             char c = res.charAt(i);
             System.out.print(c);
             if((i + 1) % 14 == 0){
                 System.out.println("。");
                 continue;
             }
             if((i + 1) % 7 == 0)
                 System.out.print(",");
         }

         System.out.println("请输入想要查找的字符串或者字符：");
         Scanner scanner = new Scanner(System.in);
         String find = scanner.nextLine();
         countString(res, find);

     }

     private static void countString(String str,String s) {
         int count = 0;
         while(str.indexOf(s) != -1){

             str = str.substring(str.indexOf(s)+1,str.length());
             count++;

         }
         System.out.println(s+"出现的次数为"+count+"次");
     }
 }


 class A{
     public static void main(String[] args) {
     
         String[] s = {"汉皇重色思倾国御宇多年求不得杨家有女初长成养在深闺人未识天生丽质难自弃一朝选在君王侧回眸一笑百媚生六宫粉黛无颜色春寒赐浴华清池温泉水滑洗凝脂侍儿扶起娇无力始是新承恩泽时云鬓花颜金步摇芙蓉帐暖度春宵春宵苦短日高起从此君王不早朝"};
         
         Lianxi.main(s);
     }
 }
 
## 4、程序截图：

![image](https://github.com/ThingKingcc/Joker/blob/master/123.png)

## 5、实验总结：

      在这次java综合性实验中，通过本学期对java所学到知识的运用，让我学到了很多很多的编程实践知识，大大提高了我对java编程和课本知识的理解。本次实验是
      
      对学生选课系统综合性编程，目的是加强我们对java所学的知识的巩固。通过分析学生选课系统，使用GUI窗体及其组件设计窗体界面，完成学生选课过程业务逻
      
      辑编程，基于文件保存并读取数据以及处理异常。在上机实习完成课程设计的过程中，遇到了不少的问题，在编写的过程中由于思路不清晰以及自己的粗心给自己
      
      制造了一些麻烦，还有就是会产生一些异常。但是在经过同学的帮助，以及自己查阅资料针对不懂得问题进行查询，再经过自己反复的检查，逐渐的得到解决，再
      
      经过自己反复的理清思路和反复的检查由思路不清晰和粗心带来的麻烦也慢慢得到了解决。
