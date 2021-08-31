---
layout: post
read_time: true
show_date: true
title: "Wrapper class"
date: 2021-08-31
img: posts/20210402/post7-header.webp
tags: [java, oop]
category: oop
author: Tuấn Anh
description: ""
toc: yes
---

Trong Java, kiểu dữ liệu được chia làm hai loại:

- Kiểu dữ liệu nguyên thuỷ (**Primitive data types**)
- Kiểu dữ liệu không nguyên thuỷ (**Non-primitive data types**). 

Thông thường, để phân biệt 2 kiểu này ta dựa vào tên của nó. Kiểu nguyên thủy có tên bắt đầu bằng chữ thường, các kiểu không nguyên thuỷ có tên bắt đầu bằng chữ in hoa. 

Ví dụ: 
- `int`, `long`, `float`, `double` là kiểu nguyên thủy
- `Integer`,`Long`, `Float`, `Double` là kiểu không nguyên thuỷ


## I. Primitive data types

Các bạn có thể đọc lại bài sau [Data types](https://github.com/AnestAcademy/Course-Java-OOP/blob/master/03.%20Data%20types.md)


## II. Non-primitive data types

### 1. Kiểu dữ liệu đối tượng

Trong java có 3 kiểu dữ liệu đối tượng:

| No |Type| Description |
|:--:|----|-------------|
|  1 | Array     | Một mảng của các dữ liệu cùng kiểu. |
|  2 | class     | Dữ liệu kiểu lớp đối tượng do người dùng định nghĩa. Chứa tập các thuộc tính và phương thức. |
|  3 | interface | Dữ liệu kiểu lớp giao tiếp do người dùng định nghĩa. Chứa các phương thức của giao tiếp. |

*Chúng ta sẽ tìm hiểu chi tiết những đối tượng này ở những bài sau.*


### 2. Wrapper class

<p align="center">
  <img src="../assets/img/posts/wrapper-class/wrapper-class.png">
</p>


Lớp Wrapper trong java cung cấp cơ chế để chuyển đổi kiểu dữ liệu nguyên thủy thành kiểu đối tượng và ngược lại từ đối tượng thành kiểu dữ liệu nguyên thủy.

| No | Kiểu nguyên thủy | Kiểu Wrapper |
|:--:|------------------|--------------|
|  1 | boolean	| Boolean   |
|  2 | char	    | Character |
|  3 | byte	    | Byte      |
|  4 | short	  | Short     |
|  5 | int	    | Integer   |
|  6 | long     | Long      |
|  7 | float	  | Float     |
|  8 | double   | Double    |


Ví dụ chuyển đổi `int` thành `Integer`:
{% highlight java %}
public class SampleClass {

    public static void main(String[] args) {
    
        int num1 = 1;
        Integer num2 = Integer.valueOf(num1);
    }
}
{% endhighlight %}


### Tại sao phải chuyển đổi kiểu dữ liệu nguyên thủy thành kiểu đối tượng?

Như chúng ta đã tìm hiểu về đối tượng, thì một đối tượng sẽ có **thuộc tính** và **phương thức** còn dữ liệu nguyên thủy thì không. Trong Java, có sẵn rất nhiều phương thức được cung cấp theo từng `class` có chức năng cụ thể để làm việc với `class` đó.

Sau khi một giá trị nguyên thủy được chuyển đổi thành đối tượng, nó có thể gọi được các phương thức của `class` đó ra để sử dụng.


<p align="center">
  <img src="../assets/img/posts/wrapper-class/wrapper-class-3.jpg">
</p>

![Wrapper Class](../assets/img/posts/wrapper-class/wrapper-class-3.jpg)


> Nếu bạn thử lấy `num1` gọi các phương thức của **class  Integer** thì chương trình sẽ báo lỗi vì `num1` là kiểu dữ liệu nguyên thủy. Nhưng sau khi chúng ta chuyển đổi `num1` thành đối tượng `num2` bằng cách sử dụng phương thức `valueOf()` được cung cấp sẵn trong **class Integer** thì `num2` có thể gọi các phương thức của **class Integer** một cách bình thường.


*Vì trong Java cung cấp rất nhiều phương thức có sẵn đi theo từng `class` nên chúng ta có thể sử dụng phím tắt `ctrl + space` trong IDE để xem nhanh danh sách phương thức được cung cấp của `class` đó.*


<p align="center">
  <img src="../assets/img/posts/wrapper-class/wrapper-class-1.jpg">
</p>


<p align="center">
  <img src="../assets/img/posts/wrapper-class/wrapper-class-2.jpg">
</p>


Ví dụ chúng ta cần tìm số `int` lớn nhất bằng bao nhiêu? Trong **class Integer** đã có sẵn thuộc tính `MAX_VALUE` lưu trữ giá trị lớn nhất của `int`, chúng ta chỉ cần gọi nó ra là xong, không cần làm gì hay tính toán gì thêm.

{% highlight java %}
public class SampleClass {

    public static void main(String[] args) {

        System.out.println(Integer.MAX_VALUE);
    }
}
{% endhighlight %}

Kết quả nhận được:
{% highlight java %}
2147483647
{% endhighlight %}


###

© Copyright
> ANEST LEARNING  
> Join us: &nbsp;&nbsp;&nbsp; [Facebook groups](https://www.facebook.com/groups/anest.learning/)  
> Website: &nbsp; [https://anest.dev](https://anest.dev)  
