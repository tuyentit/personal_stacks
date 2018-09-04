---
layout: post
title:  "Lifecycle in ASP.NET MVC"
date:   2018-09-04
categories: [dotnet]
---
**Lifecycle có gì hót?**  
Lifecycle dịch nôm na là vòng đời, vòng đời của một cái gì đó từ khi nó sinh ra, trải qua một loại các sự kiện, biến cố đến khi chết đi.

ASP.NET MVC có hai lifecycle:   
1. Application lifecycle:  
Application lifecycle tức là vòng đời của application của chúng ta từ khi được IIS (hoặc thằng self-host nào đó như console chẳng hạn) start lên rồi stop đi. Nó thể hiện bằng hai events là start, end trong startup file của MVC project.  
Bài viết này sẽ tập trung vào request lifecycle, thi thoảng đá tí sang application lifecycle.
2. Request lifecycle   
Request lifecycle là một chuỗi các event xảy ra với mỗi lần HTTP request được xử lý bởi MVC application.  
Chúng ta sẽ xem xét lại ở mức high level một lifecycle trong ASP.NET MVC
![request-lifecycle][request-lifecycle]

-> Start: Bắt đầu với một HTTP request gửi lên từ client.  
-> Routing: Request được khớp với một route được định nghĩa trong application.  
-> Request được xử lý bởi HTTP Application pipeline    
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-> Controller Initialization: Controller được khởi tạo  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-> Action Execution: MVC bắt đầu tìm kiếm và thực thi action trong controller, sau đó trả về kết quả cho bước tiếp theo (thường là JSON, XML)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;-> Result Execution: Sau bước Action Execution, kết quả trả về được xử lý với View Engine để trả về cho client bằng HTTP Response (thường là html, css)  
-> End  
 

**References:** 
* [https://www.linkedin.com/learning/asp-dot-net-mvc-http-request-life-cycle/introduction-to-the-request-life-cycle-2](https://www.linkedin.com/learning/asp-dot-net-mvc-http-request-life-cycle/introduction-to-the-request-life-cycle-2)

[request-lifecycle]:     /static/img/request-life-cycle-2.png