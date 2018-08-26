---
layout: post
title:  "Top-down vs. Bottom-up"
date:   2018-08-26
categories: [problemsolving]
---

Để giải quyết vấn đề nào đó, thường ta sẽ làm theo ba cách sau:
#### Top-down
1. Nhận vấn đề cần giải quyết, chia nhỏ nó thành các phần.
2. Tìm ra cách giải quyết cho các phần nhỏ đó.
3. Nếu phần nào to quá, ta sẽ lại tìm cách chia nhỏ thành các phần nhỏ hơn và tìm ra solution cho các phần nhỏ hơn này.
4. Kết hợp các phần đã hoàn thành với nhau.
Việc này giống như ở các dự án xây dựng vậy. Một chủ đầu tư không thể hoàn thành tất cả các công việc từ thiết kế, xây dựng, vận hành, bảo trì. Do vậy thường họ sẽ thuê/hợp tác với các đơn vị riêng rẽ về từng mảng.
Các đơn vị riêng rẽ này có thể lại thuê/hợp tác với nhiều bên khác nữa. Chủ đầu tư sẽ chịu trách nhiệm về tiến độ và chất lượng của từng mảng, sau đó khi hoàn thành thì bàn giao lại cho khách hàng.

Trong lập trình, chúng ta cũng gặp concept này ở mọi nơi.
Muốn hoàn thành dự án X, chúng ta chia thành x modules, sau đó giao cho các module này về các team nhỏ như team làm design, team làm front end, team làm backend, hoặc team fullstack luôn :))
Hoặc chúng ta muốn code hàm nào đó, chúng ta chia hàm thành các hàm nhỏ hơn, dễ bảo trì, maintain và unit test được.
Cách này mình thấy sẽ rất hiệu quả khi mà mình đã clear solution ở một mức độ nào đó.

#### Bottom-up
Việc này ngược lại với mindset ở trên.
Chúng ta tìm ra những mảnh nhỏ để giải quyết vấn đề. Sau đó hợp nhất chúng tại để hoàn thành những mảng lớn hơn.
Cách này rất hiệu quả khi mà mình chưa có solution thực sự, đang mò mẫm.
Ví dụ chúng ta nhận một công việc research nào đó, chúng ta đều là newbie trong lĩnh vực này. Thì việc mò mẫn là điều hiển nhiên, chúng ta không đủ nhận thức để đi theo hướng top-down.

#### Mixed
Có một điều mình nhận thấy rằng, khi fixed mindset của mình rằng phải đi theo bottom-up hay top-down thì làm việc khá cứng nhắc. Sự linh hoạt trong cách tiếp cận là một điều cần thiết.
Tuy nhiên, mình nhận thấy có rất nhiều bạn ít khi nghĩ về cách làm việc, nên mixed cách tiếp cận một cách không khoa học và không có sắp xếp, dẫn tới công việc khá lộn xộn và chất lượng không được như ý.
Một số ví dụ rất thường gặp như:

* Khi một bạn code một chức năng lớn hay những method dài, nếu không có cách tiếp cận, sẽ dẫn đến việc chia  method, khai báo các parameters của method rất lộn xộn. Khó đọc, không có readable. Những bạn này thường code theo kiểu cần đâu code đó, thiếu gì thêm đó, cứ else if switch case mọi nơi. Người review code thì rất khó để đi theo con đường các bạn đã vẽ ra trong những dòng code (flow). Các method thì thường rất khó để UT vì nó phụ thuộc chồng chéo.  

* PM giao một đống tasks cho members, sau một hồi làm, cả team cứ thấy task cứ dài lê thê, bug phần nọ dây sang phần kia, mà không thấy một progress gì rõ ràng về tiến độ dự án cả (bạn PM đã không top-down ở đây). Việc này rất hay gặp vì rất nhiều bạn đi lên quản lý do bạn ý code rất siêu. Tuy nhiên những kỹ năng về quản lý & phân chia tasks chưa tốt.

*Điều mình muốn nhắn nhủ là khi gặp vấn đề hãy nghĩ đến cách tiếp cận vấn đề chứ đừng nhảy vào giải quyết luôn. Work smart một xíu ;)*