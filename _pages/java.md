---
title: Java语法
author: Zhang
date: 2022-08-01
category: code
layout: post
---



```java
// this的本质：代表方法调用者的地址值

// 
StringJoiner stj = new StringJoiner(",");
stj.add("大张");
stj.add("Java");
stj.add("笔记");
System.out.println(stj);

// == or equals
x==y
x.equals(y)

// Iterator
List<String> list = new ArrayList<>();
list.add("aaa");
list.add("bbb");

Iterator<String> it = list. iterator();
while(it.hasNext()){
    String obj = it.next();
    System.out.println(obj);
}

// generics
public class GenericClass<T> {
    private T value;

    public GenericClass(T value) {
        this.value = value;
    }

    public T getValue() {
        return value;
    }

    public void setValue(T value) {
        this.value = value;
    }

    public static void main(String[] args){

        GenericClass<String> name = new GenericClass<>("大张Java笔记");
        System.out.println(name.getValue());

        GenericClass<Integer> number = new GenericClass<>(123);
        System.out.println(number.getValue());
    }
}

// swing
import javax.swing.*;
import java.awt.event.*;
import javax.swing.JOptionPane;
public class server
{
    public static void main(String[] args) {
        JFrame jFrame = new JFrame("title");
        JPanel jPanel = new JPanel();
        JButton button = new JButton("Test button");
        button.addActionListener(new ActionListener() {
            public void actionPerformed(ActionEvent e) {
                JOptionPane.showMessageDialog(null,"恭喜，登录成功！","提醒",JOptionPane.INFORMATION_MESSAGE);
            }
        });

        jPanel.add(button);
        jFrame.setContentPane(jPanel);
        jFrame.setSize(300,300);
        jFrame.setLocationRelativeTo(null);
        jFrame.setVisible(true);
        jFrame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
    }
}
```
```java
// HelloWorld.java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello world!");
    }
}
```
