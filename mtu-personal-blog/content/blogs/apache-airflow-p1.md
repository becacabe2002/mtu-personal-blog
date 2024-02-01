---
title: 'Introduction to Apache Airflow | Airflow Part 1'
date: 2024-02-01T13:48:41+07:00
lastMod: 2024-02-01T13:48:41+07:00
tocopen: false
description: "Bài đầu tiên trong chuỗi series tìm hiểu về Apache Airflow."
summary: "Bài đầu tiên trong chuỗi series tìm hiểu về Apache Airflow."
tags: ["airflow", "data", "orchestration"]
cover:
    image: "/images/airflow/airflow-cover.png"
    alt: "alt text"
    relative: false
---

## Định nghĩa 
> _**Apache Airflow** là một nền tảng mã nguồn mở để phát triển, lập lịch và giám sát luồng công việc của các project dữ liệu._ 

* Airflow hỗ trợ giao diện web giúp quản lý các trạng thái (state) của luồng công việc một cách trực quan. 

![web interface](/images/airflow/airflow-dashboard.png)

* Ta có thể triển khai Airflow trên nhiều nền tảng, từ local trên máy tính cá nhân, tới hệ phân tán được setup để hỗ trợ luồng công việc khổng lồ.

### Một số đặc tính nổi bật của Airflow

* **Dynamic**: các pipeline trong Airflow được cấu hình động bằng việc sử dụng Python code.

* **Extensible**: Airflow framework có chứa các operators, cho phép kết nối với các công nghệ khác (**_Astronomer_**, **_Grafana_** ...)

* **Flexible**: tính linh hoạt của luồng hoạt động nhờ tận dụng **_Jinja_** template

### Vì sao nên dùng Airflow?

* Với những workflow có khởi đầu và kết thúc rõ ràng, ta có thể cấu hình chúng thành các Airflow DAG (sẽ được giới thiệu sau)

* Workflow được định nghĩa thành Python code, cho phép:
    * Workflows có thể được quản lý phiên bản, cho phép rollback phiên bản cũ.
    * Workflows có thể được phát triển bởi nhiều người trong một team.
    * Có thể tạo các test để kiểm tra các chức năng

* Airflow cho phép lập lịch các task, giúp tạo các pipeline phức tạp. Ngoài ra, khả năng chạy lại một phần pipeline sau khi khác phục sự cố giúp tối đa hóa hiệu suất.

* Giao diện người dùng của Airflow cung cấp:
    * Góc nhìn chi tiết: Pipelines, Tasks
    * Góc nhìn tổng quan hoạt động của các pipelines theo thời gian
    * Inspect logs và khởi chạy task trong trường hợp chạy lỗi

* Airflow là mã nguồn mở, cho phép tính tùy biến cao. Do đó được tin dùng bởi nhiều công ty trên thế giới.

### Những trường hợp nào không nên dùng Airflow?

* Airflow không hỗ trợ các luồng công việc không ngừng dựa trên sự kiện.
    * Mặc dù Airflow hỗ trợ Apache Kafka, là một streaming system được sử dụng để tiếp nhận và sử lý dữ liệu thời gian thực. Nhưng các task sẽ được tái khởi động định kì.

* Không phù hợp với nếu người dùng ưu việc chọn thay vì code.

