Q1)Write a program to create a class and implement default,overloaded,copy constuctor
A)
#DEFAULT 
public class Bike {
    Bike(){
        System.out.print("Bike Is Created");
    }

    public static void main(String[] args) {
        Bike b=new  Bike();
    }
}
#OVERLOADED
public class Add {
Add () {
System.out.println("Hiiii");
}
Add(int a) {
System.out.println("a="+a);
}
Add(char c) {
System.out.println("c="+c);
}
public static void main(String[] args) {
Add obj1=new Add();
Add obj2=new Add(10);
Add obj3=new Add('@');
}
}
#COPY
public class Student1 {
int id;
String name;
Student1(int i, String n) {
id=i;
name=n;
}
Student1(Student1 s) {
id=s.id;
name=s.name;
}
void display () {
System.out.println(id+"      "+name);
}
public static void main(String[] args) {
Student1 s1=new Student1 (111,"Karan");
Student1 s2=new Student1(s1);
s1.display();
s2.display();
}
}
B)OVERLOADING
public class Addition {
void add(){
System.out.println("Zero parameter");
}
void add(char a) {
    System.out.println("character="+a);
}
void add(int a, int b) {
System.out.println("a="+a+"b="+b);
}
void add(int e, float d) {
System.out.println("e="+e+"d="+d);
}
public static void main(String[] args) {
Addition a=new Addition();
a.add();
a.add('@');
a.add(10,20);
a.add(50,60.5F);
}
}
C)STATIC
public class Number {
static void greatest() {
int x=10;
int y=20;
if (x>y) {
System.out.println("X is greatest");
}
else{
System.out.println("Y is greatest");
}
return;
}
public static void main(String[] args) {
Number.greatest();
}
}


Q2)Write a program to implement the concept of Inheritance and method overriding
#INHERITANCE
class Employee {
float salary=40000;
}
public class Programmer extends Employee {
int bonus=10000;
public static void main(String[] args) {
Programmer p = new Programmer();
System.out.println("Programmer salary is: "+p.salary);
System.out.println("Bonus of Programmer is: "+p.bonus);
}
}
#SINGLE INHERITANCE
class Animal {
void eat () {
System.out.println("Eating.....");
}
}
Class Dog extends Animal {
void bark() {
System.out.println("Barking........ ");
}
}
public class Test inheritance {
public static void main(String[] args) {
Dog d=new Dog();
d.bark();
d.eat();
}
}
#MULTIPLE INHERITANCE
class Animal {
void eat (){
System.out.println("Eating.......");
}
}
class Dog extends Animal{
void bark() {
System.out.println("Barking......");
}
}
class BabyDog extends Dog{
void weep(){
System.out.println("Weeping......");
}
}
public class Testinheritance2 {
public static void main(String[] args) {
BabyDog d=new BabyDog();
d. weep();
d.bark();
d.eat();
}
}
#HIERARCHIAL INHERITANCE
class Animal {
void eat () {
System.out.println("Eating...");
}
}
class Dog extends Animal {
void bark() {
System.out.println("Barking...");
}
}
class Cat extends Animal {
void meow() {
System.out.println("Meowing......");
}
}
public class Testinheritance3 {
public static void main(String[] args) {
Cat c=new Cat();
c.meow();
c.eat();
}
}
#METHOD OVERRIDING
class Bank{
int getRateOfInterest () {
return 0;
}
}
class SBI extends Bank{
int getRateOfInterest () {
return 8;
}
}
class ICICI extends Bank{
int getRateOfInterest () {
return 7;
}
}
class AXIS extends Bank{
int getRateOfInterest () {
return 9;
}
}
public class Test2 {
public static void main(String[] args) {
SBI s=new SBI();
ICICI i=new ICICI();
AXIS a=new AXIS();
System.out.println("SBI Rate Of Interest: "+s.getRateOfInterest());
System.out.println("ICICI Rate Of Interest: "+i.getRateOfInterest());
System.out.println("AXIS Rate of Interest: "+a.getRateOfInterest());
}
}
#B)Write a program to implement the concepts of Abstract classes and
methods.
abstract class Bike {
abstract void run();
}
public class Honda4 extends Bike {
void run() {
System.out.println("running safely...");
}
public static void main(String[] args) {
Bike obj=new Honda4();
obj.run();
}
}
#C)Write a program to implement the concept of Interfaces.
interface Drawable {
void draw();
}
class Rectangle implements Drawable {
public void draw() {
System.out.println("Drawing Rectangle");
}
}
class Circle implements Drawable {
public void draw() {
System.out.println("Drawing Circle");
}
}
public class Testinterfacel1{
public static void main(String[] args) {
Drawable d=new Circle();
d.draw();
}
}


Q3)
A)Write a program to raise built-in exception and raise them as per the
requirements.
import java.io.*;
public class Divide {
public static void main(String[] args) throws IOException {
int a,b,res;
BufferedReader br=new BufferedReader(new InputStreamReader(System.in));
String str;
System.out.println("Enter two numbers:");
str=br.readLine();
a=Integer.parseInt(str);
str=br.readLine();
b=Integer.parseInt(str);
res=a/b;
System.out.println("The Quotient="+res);
}
}
B)Write a program to define user defined exceptions and raise them as per
the requirements.
import java.io.*;
public class Divide12 {
public static void main(String[] args) throws IOException{
int a=0,b=0,res;
BufferedReader br=new BufferedReader(new InputStreamReader(System.in));
String str;
System.out.println("Enter two numbers:");
try{
str=br.readLine();
a=Integer.parseInt(str);
str=br.readLine();
b=Integer.parseInt(str);
try{
res=a/b;
System.out.println("The Quotient="+res);
}
catch (ArithmeticException ae) {
System.out.println("Exception has occured. You have entered the divisor as zero");
}
}
catch (NumberFormatException ne) {
System.out.println("Invalid Number");
}
}
}


Q4)SWINGGS
A)write a java program to create a frame using inheritance in swing
import javax.swing.JFrame;
public class GridLayout extends JFrame {
GridLayout() {
setSize(400,600);
setLayout(null);
setVisible(true);
}
public static void main(String[] args) {
GridLayout obj=new GridLayout();
}
}
B)write a java program to create a frame using Association in swing
import javax.swing.JFrame;
public class GridLayout {
GridLayout () {
JFrame f=new JFrame();
f.setSize(400,600);
f.setLayout(null);
f.setVisible(true);
}
public static void main(String[] args) {
GridLayout obj=new GridLayout();
}
}


Q5) LAYOUTS
A)GRID LAYOUT
import java.awt.GridLayout;
import javax.swing.*;
public class GridLayout extends JFrame{
    JLabel l1,l2;
    JTextField t1;
    JButton b1;
    GridLayout()
    {
        l1=new JLabel("Name");
        l2=new JLabel();
        t1=new JTextField();
        b1=new JButton("Submit");
        add(l1);
        add(t1);
        add(l2);
        add(b1);
        setSize(400,600);
        setLayout (new GridLayout (2,2));
        setVisible(true);
}
    public static void main(String[] args) {
        GridLayout obj=new GridLayout();
    }
    
}
B)FLOW LAYOUT
import java.awt.FlowLayout;
import javax.swing.*;
public class FlowLayout1 extends JFrame{
    JLabel l1,l2;
    JTextField t1;
    JButton b1;
    FlowLayout1()
    {
        l1=new JLabel("Name");
        l2=new JLabel();
        t1=new JTextField();
        b1=new JButton("Submit");
        add(l1);
        add(t1);
        add(l2);
        add(b1);
        setSize(400,600);
        setLayout (new FlowLayout());
        setVisible(true);
}
    public static void main(String[] args) {
        FlowLayout1 obj=new FlowLayout1();
    }
    
}
C)BORDER LAYOUT
import java.awt.BorderLayout;
import javax.swing.*;
public class BLayout extends JFrame{
    JButton b1,b2,b3,b4,b5;
    BLayout()
    {
        b1=new JButton("North");
        b2=new JButton("South");
        b3=new JButton("East");
        b4=new JButton("West");
        b5=new JButton("Center");
        add(b1,BorderLayout.NORTH);
        add(b2,BorderLayout.SOUTH);
        add(b3,BorderLayout.EAST);
        add(b4,BorderLayout.WEST);
        add(b5,BorderLayout.CENTER);
        setSize(400,600);
        setVisible(true);
    }
    public static void main(String[] args) {
        BLayout obj=new BLayout();
    }
    
}


Q6)Events
A)write a java program to demonstrate the ActionEvent and take the name from uuser and display the messagge
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import javax.swing.*;
public class Events extends JFrame implements ActionListener{
JLabel l1,l2;
JTextField t1;
JButton b1;
Events(){
    l1=new JLabel("Name");
    t1=new JTextField();
    b1=new JButton("Display");
    l2=new JLabel();
    b1.addActionListener(this);
    add (l1);
    add (t1);
    add (b1);
    add (l2);
    setSize (300,300);
    setLayout (new GridLayout (2,2));
    setVisible(true);
}
    public static void main(String[] args) {
        Events obj=new Events();
    }
    @Override
    public void actionPerformed(ActionEvent e) {
        String n=t1.getText();
        l2.setText("Welcome "+n);
    }
}
6B)write a java program to demonstrate the ActionEvent and take two numbers from users and display the addition
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import javax.swing.*;
public class Events extends JFrame implements ActionListener{
JLabel l1,l2;
JTextField t1,t2,t3;
JButton b1;
Events(){
    l1=new JLabel("Number1");
    l2=new JLabel("Number2");
    b1=new JButton("Result");
    t1=new JTextField();
    t2=new JTextField();
    t3=new JTextField();
    b1.addActionListener(this);
    add (l1);
    add (t1);
    add (l2);
    add (t2);
    add (b1);
    add (t3);
    setSize (300,300);
    setLayout (new GridLayout (3,3));
    setVisible(true);
}
    public static void main(String[] args) {
        Events obj=new Events();
    }
    @Override
    public void actionPerformed(ActionEvent e) {
       int a=Integer.parseInt(t1.getText());
       int b=Integer.parseInt(t2.getText());
       int c=a+b;
       t3.setText(" "+c);
    }
}


Q7)Demonstrate the use of Anonymous inner class in Event Handling
import java.awt.*;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import javax.swing.*;
public class Events extends JFrame {
JLabel l1,l2;
JTextField t1;
JButton b1;
Events(){
    l1=new JLabel("Name");
    t1=new JTextField();
    b1=new JButton("Display");
    l2=new JLabel();
    b1.addActionListener(new ActionListener()
    {
        @Override
       public void actionPerformed(ActionEvent e) {
        String n=t1.getText();
        l2.setText("Welcome" +n);
    }
    });
    add(l1);
    add(t1);
    add(b1);
    add(l2);
    setSize (300,300);
    setLayout (new GridLayout(2,2));
    setVisible(true);
}
    public static void main(String[] args) {
        Events obj=new Events();
    }
}


    

