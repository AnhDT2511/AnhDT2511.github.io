---
layout: post
read_time: true
show_date: true
title: "OOP in Java"
date: 2021-08-28
description: "ELI5: what is a neural network."
img: posts/20210402/post7-header.webp
tags: [java, oop, basic]
category: oop
author: Tuấn Anh
github: AnestAcademy/Course-Java-OOP/blob/master/06.%20OOP%20in%20Java.md
---

Lập trình hướng đối tượng **(Object Oriented Programming – OOP)** là một trong những kỹ thuật lập trình rất quan trọng và sử dụng nhiều hiện nay. Hầu hết các ngôn ngữ lập trình hiện nay như Java, PHP, .NET, Ruby, Python... đều hỗ trợ OOP.


## I. What is OOP

**Lập trình hướng đối tượng (OOP)** là một kỹ thuật lập trình cho phép lập trình viên tạo ra các đối tượng trong code - trừu tượng hóa các đối tượng trong cuộc sống vào trong code để tương tác - tính toán - xử lý.


## II. OOP in programming

Giả sử bạn đang muốn tạo ra một chiếc ô tô, vậy trước tiên bạn cần thiết kế ra một bản thiết kế của cái ô tô đó. Trong bản thiết kế đó sẽ phác thảo ra những thông tin, đặc điểm của chiếc ô tô cần có ví dụ như: tên, màu sắc, kích thước, trọng lượng... bên cạnh đó bạn cũng cần phải mô tả được những công dụng, thao tác, hành động mà chiếc ô tô đó có thể làm được.

Và khi bạn đã có bản thiết kế thì bạn có thể tạo ra chiếc ô tô, chiếc ô tô này sẽ có các đặc điểm và hành động giống y bản thiết kế.

Như trong cuộc sống, bạn chỉ cần có một bản thiết kế nhưng không vì vậy mà chỉ tạo được một chiếc ô tô - bạn có thể tạo ra được rất nhiều chiếc ô tô dựa trên một bản thiết kế và tất cả chiếc ô tô được tạo ra cùng một bản thiết kế thì đều có các đặc điểm và hành động giống nhau. Nhưng giá trị của những thông tin, đặc điểm sẽ có thể khác nhau hoặc trùng nhau ví dụ: có chiếc xe màu đỏ, có chiếc màu xanh, màu trắng...

Mỗi chiếc ô tô tạo ra được xem là một thực thể (có thực, đã được tạo ra trong thực tế) thể hiện của bản thiết kế.


### 1. Class

Vậy `class` trong Java là gì? Nó được xem như là một bản thiết kế các đối tượng (object) trong lập trình.

Một `class` là một kiểu dữ liệu (data type) bao gồm:
- `thuộc tính (Property - Attribute)`: thể hiện qua biến (variable)
- `phương thức (Method)`: thể hiện qua hàm (function)
được định nghĩa từ trước. 

Khác với kiểu dữ liệu thông thường (nguyên thủy), một `class` là một đơn vị (trừu tượng) bao gồm sự kết hợp giữa các `thuộc tính` và các `phương thức`. 


### 2. Object

`class` bạn có thể hiểu nó như là khuôn mẫu, bản thiết kế thì `object` là một thực thể thể hiện (instance) dựa trên khuôn mẫu đó. Hay như ở bối cảnh trên, `object` chính là những chiếc ô tô được tạo ra từ bản thiết kế.

> Trong lập trình, mặc định các `object` là khác nhau cho dù có cùng các giá trị `thuộc tính` và `phương thức` giống nhau.


## III. What are the main principles of OOP

Lập trình hướng đối tượng có 4 tính chất đặc thù sau:

- Tính đóng gói (Encapsulation)
- Tính kế thừa (Inheritance)
- Tính đa hình (Polymorphism)
- Tính trừu tượng (Abstraction)

Khái niệm cơ bản:

- **Tính đóng gói** nhằm bảo vệ đối tượng không bị truy cập từ code bên ngoài vào để thay để giá trị các thuộc tính hay có thể truy cập trực tiếp. Việc cho phép truy cập các giá trị của đối tượng tùy theo sự đồng ý của người viết ra lớp của đối tượng đó. Tính chất này đảm bảo sự bảo mật, toàn vẹn của đối tượng trong Java.

- **Tính kế thừa** cho phép chúng ta cải tiến chương trình bằng cách kế thừa lại lớp cũ và phát triển những tính năng mới. Lớp con sẽ kế thừa tất cả những thành phần của lớp cha, nhờ sự chia sẻ này mới có thể mở rộng những đặc tính sẵn có mà không cần phải định nghĩa lại.

- **Tính đa hình** có thể nói luôn tồn tại song song với tính kế thừa. Khi có nhiều lớp con kế thừa lớp cha nhưng có những tính chất khác nhau cũng gọi là đa hình, hoặc những tác vụ trong cùng một đối tượng được thể hiện nhiều cách khác nhau cũng gọi là đa hình. Tính đa hình là kết quả tất yếu khi ta phát triển khả năng kế thừa và nâng cấp chương trình.

- **Tính trừu tượng** là một tiến trình chỉ nói ra tính năng của người dùng, các khái niệm được định nghĩa trong quá trình phát triển, bỏ qua những chi tiết triển khai bên trong. Tính trừu tượng cho phép người lập trình tập trung cốt lõi cần thiết của đối tượng thay vì quan tâm sự phức tạo bên trong hoặc cách nó hoạt động.

Trong các bài sau, chúng ta sẽ đi sâu và giải thích rõ hơn từng tính chất cụ thể ở trên và thực hiện code ví dụ minh họa - để có thể hiểu được những tính chất trên được thể hiện trong code như thế nào.


## IV. Advantages of object-oriented programming

- Dựa trên nguyên lý kế thừa, trong quá trình tạo - mô tả các `class` có thể loại bỏ những chương trình bị lặp, dư. Và có thể mở rộng khả năng sử dụng các `class` mà không cần thực hiện lại. Tối ưu và tái sử dụng code hiệu quả.
- Đảm bảo rút ngắn thời gian xây dựng hệ thống và tăng năng suất thực hiện.
- Sự xuất hiện của 2 khái niệm mới là `class` và `object` chính là đặc trưng của phương pháp lập trình hướng đối tượng. Nó đã giải quyết được các khuyết điểm của phương pháp lập trình hướng cấu trúc để lại. Ngoài ra 2 khái niệm này đã giúp biểu diễn tốt hơn thế giới thực trên máy tính.


###

© Copyright
> ANEST LEARNING  
> Join us: &nbsp;&nbsp;&nbsp; [Facebook groups](https://www.facebook.com/groups/anest.learning/)  
> Website: &nbsp; [https://anest.dev](https://anest.dev)  
