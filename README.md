# SHIYAN3
学生选课系统
# java-lesson
for java experiment2


## 实验目的
初步了解分析系统需求，从学生选课角度了解系统中的实体及其关系，学会定义类中的属性以及方法；

掌握面向对象的类设计方法（属性、方法）；

掌握类的继承用法，通过构造方法实例化对象；

学会使用super()，用于实例化子类；

掌握使用Object根类的toString（）方法,应用在相关对象的信息输出中。


## 实验方法
1.阅读需求，明白创建的类，变量及其方法

2.分类分别编写teacher people student lesson等几类

3.写出所需信息，进行编译。

4.调试并修改代码，使其正常运行，达到实验目的。

## 实验过程
1.创建project，并在其下创建package xueshenxuanke，在package下创建class，根据需求分别将各部分功能写入。

2.在类中创建变量，是其一一对应。

3.name number sex等信息一一表示出来。

4.检查变量名有无错误以及是否对应。

5.检查方法是否有误。

## 核心方法
'''
class People{
    public People(){

    }
    public People(String name,int age,int number,String sex){
        this.name = name;
        this.age = age;
        this.number = number;
        this.sex = sex;
    }

    private String name;
    private int age;
    private int number;
    private String sex;

    public String getName() {
        return name;
    }
    public int getAge() {
        return age;
    }
    public String getSex() {
        return sex;
    }
    public int getNumber() {
        return number;
    }
    public void setName(String name) {
        this.name = name;
    }
    public void setAge(int age) {
            this.age = age;
    }
    public void setNumber(int number) {
        this.number = number;
    }
    public void setSex(String sex) {
        this.sex = sex;
    }

}

class Student extends People{
    public Student(){

    }
    public Student(String name,int age,int number,String sex){
        super(name, age, number, sex);
    }
}

class Teacher extends People{
    public Teacher(){

    }
    public Teacher(String name,int age,int number,String sex){
        super(name, age, number, sex);
    }
    String lesson_1;
    public String getLesson_1() {
        return lesson_1;
    }
    public void setLesson_1(String lesson_1) {
        this.lesson_1 = lesson_1;
    }


}


class Lesson{
    public Lesson(){

    }
    public Lesson(String name,String time,int number,String place){
        this.name = name;
        this.time = time;
        this.number = number;
        this.place = place;
    }

    private String name;
    private String time;
    private int number;
    private String place;


    public String getName() {
        return name;
    }
    public String getTime() {
        return time;
    }

    public String getPlace() {
        return place;
    }
    public int getNumber() {
        return number;
    }
    public void setName(String name) {
        this.name = name;
    }
    public void setTime(String time) {
        this.time = time;
    }
    public void setNumber(int number) {
        this.number = number;
    }
    public void setPlace(String place) {
        this.place = place;
    }

}


class Lesson_1 extends Lesson{
    public Lesson_1(){

    }
    public Lesson_1(String name,String time,int number,String place){
        super(name, time, number, place);
    }
    public String toString() {
        return "课程名称：" + getName()+ "\n" + "上课时间：" + getTime() + "\n" + "课程编号：" + getNumber()+ "\n" + "授课地点：" + getPlace()+ "\n";
    }
}

通过class分类把被选课老师，学生，课程编号，上课时间，授课地点等信息都表示出来，使信息更加清楚明白。
'''

## 实验结果
******************学生信息*********************
学生姓名:李建涛
学生年龄:20
学生编号:2019310857
学生性别:男

******************教师信息*********************
授课教师:董小燕
教师年龄:35
教师编号:2001700001
教师性别:女

******************课程信息*********************
课程名称：概率
上课时间：每周三 下午4:05-5:40
课程编号：1234567
授课地点：教203


******************课程详情*********************
诸位同仁选课成功，快乐的学习就要开始了

## 实验感想
通过这次实验，我懂得了类的重要性和分类的必要，对super访问父类属性和extends继承父类构造方法有了解，明白了这种分类的意义,通过一次次的实验让我懂得java算法的重要性。
