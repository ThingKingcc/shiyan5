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


package school;

public class Student extends Personal {


	private Course course;
	private Teacher teather;
	
	public Course getCourse() {
		return course;
	}
	public void setCourse(Course course) {
		this.course = course;
	}
	public Teacher getTeather() {
		return teather;
	}
	public void setTeather(Teacher teather) {
		this.teather = (Teacher) teather;
	}
	public void putcourse(){
		if(course==null){
			System.out.println("Not to choose course");
		}else{
		this.toString();
		}
	}
	public String toString(){
	
//		System.out.println("Student toString is operating");
		return id+name+sex+course+teather.getName();
	}
		
	
	public Student(int id, String name, String sex,Course course,Teacher teather) {
		super(id, name, sex);
		
			this.course=course;
			this.teather=teather;
		
	
	}
	public Course delete() {
		return course=null;
	}


package school;

import java.awt.Button;
import java.awt.Color;
import java.awt.FlowLayout;
import java.awt.Frame;
import java.awt.TextField;
import java.awt.Window;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.awt.event.WindowAdapter;
import java.awt.event.WindowEvent;


public class TestFlowLayout {

    public static void main(String[] args) {

    	 Frame f = new Frame();//建立一个空窗口。
    	 f.setTitle("Frame WHERECOME du");
    	 FlowLayout fl = new FlowLayout();  //使用流布局
         f.setLayout(fl);//修改布局管理
         f.setSize(500, 400);//设置窗口大小,
         f.setLocation(300, 200);//设置窗口的初始位置
         f.setVisible(true);//显示窗口。
    	 

         f.addWindowListener(new WindowAdapter(){
 			public void windowClosing(WindowEvent e){
 				Window window=(Window)e.getComponent();
 				window.dispose();
 			}
 		});


 		TextField textField = new TextField();
 		textField.setBounds(200, 100, 200, 50);
 		textField.setBackground(Color.white);
 		MyActionListener myActionListener = new MyActionListener(textField);//创建一个按钮监听事件对象
 		f.add(textField);
 		Button button1= new Button("Choose couse");
 		Button button2= new Button("Back course");
 		button1.setBounds(100,100,100,100);
 		button1.setBackground(Color.orange);
 		button1.addActionListener(myActionListener);//添加myActionListener监听事件
 		f.add(button1);

 		button2.setBounds(300,300,300,300);
 		button2.setBackground(Color.red);
 		ActionListener myActionListener2=new MyActionListener2(textField);
		button2.addActionListener(myActionListener2);//添加myActionListener监听事件
 		f.add(button2);
        f.setLayout(null);//清空布局
    }
    	
}
class MyActionListener implements ActionListener{
	
	 Course course=new Course(1, "Java", "综合楼",3,3);
	 Teacher teather=new Teacher(1, "张世博", "男",course);
	 Student student=new Student(1, "陈玺庆", "男",course,teacher);
	private TextField textField;
 
	public MyActionListener(TextField textField) {
		super();
		this.textField = textField;
	}
	public void actionPerformed(ActionEvent e) {
		textField.setText(" " +student+ " ");
}
}
class MyActionListener2 implements ActionListener{
	
	private TextField textField;
	public MyActionListener2(TextField textField) {
		super();
		this.textField = textField;
	}
	public void actionPerformed(ActionEvent e) {
			textField.setText("not to chouse course");
	
	}
	
}

## 4、程序截图：

![image](https://github.com/ThingKingcc/shiyan5/blob/master/a.png)
![image](https://github.com/ThingKingcc/shiyan5/blob/master/b.png)

## 5、实验总结：

      在这次java综合性实验中，通过本学期对java所学到知识的运用，让我学到了很多很多的编程实践知识，大大提高了我对java编程和课本知识的理解。本次实验是
      
      对学生选课系统综合性编程，目的是加强我们对java所学的知识的巩固。通过分析学生选课系统，使用GUI窗体及其组件设计窗体界面，完成学生选课过程业务逻
      
      辑编程，基于文件保存并读取数据以及处理异常。在上机实习完成课程设计的过程中，遇到了不少的问题，在编写的过程中由于思路不清晰以及自己的粗心给自己
      
      制造了一些麻烦，还有就是会产生一些异常。但是在经过同学的帮助，以及自己查阅资料针对不懂得问题进行查询，再经过自己反复的检查，逐渐的得到解决，再
      
      经过自己反复的理清思路和反复的检查由思路不清晰和粗心带来的麻烦也慢慢得到了解决。
