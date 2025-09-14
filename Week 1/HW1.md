# Homework 1

***

## Docker, docker compose là gì?

### Docker là gì?

#### Khái niệm

* Docker là một nền tảng mã nguồn mở giúp người dùng xây dựng, đóng gói, phân phối và chạy ứng dụng trong một môi trường được gọi là *container*

* Mỗi container chứa đầy đủ những thứ để một ứng dụng chạy được: mã nguồn, thư viện phụ thuộc, môi trường thực thi, cấu hình và các công cụ cần thiết. Như vậy, ứng dụng sẽ chạy như nhau dù trên máy tính người phát triển, máy chủ thử nghiệm hoặc máy chủ sản xuất.

* Có thể nói, container giống như một hộp chứa ứng dụng và mọi thứ nó cần. Docker là công cụ để tạo ra chiếc hộp này, quản lí chúng, di chuyển chúng dễ dàng giữa các máy.

#### Công dụng

* Docker đóng gói mọi thứ trong container một cách nhất quán để tránh trường hợp chạy được trên máy này nhưng không chạy được trên máy khác do version khác, cấu hình khác, môi trường khác nhau.

* Docker cho phép cô lập ứng dụng với môi trường của nó để giúp quản lí nhiều phụ thuộc lằng nhằng khi nhiều ứng dụng, công nghệ khác nhau trên cùng một máy chủ.

#### Một số khái niệm liên quan

* *image*: là khuôn mẫu (template) để tạo ra container. Một image chứ mã nguồn ứng dụng, thư viện, dependencies, cấu hình,... Từ image, người dùng sẽ tạo container để chạy ứng dụng.

* *container*: là phiên bản đang chạy của image. Container giống như một hộp thực sự, trong đó ứng dụng chạy độc lập với các hộp khác. Một image có thể tạo ra nhiều container giống hệt nhau.

* *Dockerfile*: là tập tin văn bản chứa các lệnh để Docker biết cách build ra 1 image.

### Docker-compose là gì?

#### Khái niệm

* Docker Compose là một công cụ đi kèm Docker (cài sẵn hoặc có thể cài thêm), cho phép người dùng định nghĩa và quản lý nhiều container cùng lúc bằng một file cấu hình YAML (docker-compose.yml).

#### Công dụng

* Docker Compose cho phép quản lí nhiều container như một ứng dụng. Trong thực tế, ứng dụng hiếm khi chỉ có một thành phần, ví dụ như web server, database, cache, message queue,... Vì vậy, docker compose cho phép gom tất cả thành một ứng dụng duy nhất.

## Linux vs Unix vs BSD vs *nix? macOS thuộc loại nào?

### Unix

#### Khái niệm

Unix là một hệ điều hành được phát triển lần đầu tiên vào thập kỉ 60 và phát triển không ngừng kể từ đó. Đây là một hệ thống ổn định, đa người dùng, đa tác vụ cho máy chủ, máy tính để bàn và máy tính xách tay.

#### Một số đặc điểm chính







