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

Unix là họ hệ điều hành máy tính đa nhiệm, đa người dùng, được phát triển từ khoảng cuối những năm 1960 và đầu những năm 1970 tại Bell Labs (AT&T) bởi Ken Thompson, Dennis Ritchie, Douglas McIlroy, và những người khác.

#### Một số đặc điểm chính

* Đa người dùng (multi-user) và đa nhiệm (multitasking).

* Triết lý Unix: các công cụ nhỏ, mỗi công cụ làm một việc, được kết hợp bằng shell/ line lệnh và pipes.

* Di động cao - Unix được viết chủ yếu bằng ngôn ngữ C, vì vậy dễ port sang các kiến trúc phần cứng khác nhau.

### BSD

#### Khái niệm

BSD (Berkeley Software Distribution) là một nhánh dẫn xuất từ Unix, được xây dựng tại Đại học California, Berkeley, vào thập niên 1970. Nó ban đầu là tập hợp các bản mở rộng của Unix, sau phát triển thành hệ điều hành độc lập với nhiều biến thể như FreeBSD, NetBSD, OpenBSD…

##### Một số đặc điểm chính

* Là dẫn xuất từ Unix nên được thừa hưởng nhiều đặc điểm của Unix.

* Có phiên bản mã nguồn mở (free/open source), giấy phép BSD cho phép dễ dàng sử dụng lại trong cả phần mềm thương mại.

* Có nhiều biến thể chuyên biệt: FreeBSD, NetBSD, OpenBSD,...

### Linux

#### Khái niệm

Linux là nhân (kernel) do Linus Torvalds phát triển năm 1991, đi kèm với các phần mềm hỗ trợ (như GNU), tạo thành các bản phân phối Linux. Linux tương tự Unix về cách hoạt động (Unix-like), nhưng mã nguồn được xây dựng lại, không từ code Unix gốc.

#### Một số đặc điểm chính

* Mã nguồn mở, được phân phối dưới nhiều bản phân phối khác nhau, người dùng có nhiều lựa chọn.

* Tương tự Unix về nhiều mặt: hỗ trợ đa nhiệm, đa người dùng, hệ thống file kiểu Unix, networking mạnh.

* Tính phổ biến cao, được sử dụng rộng rãi.

### *nix

#### Khái niệm:

* Đây là cách gọi chung cho các hệ điều hành "giống Unix" (*nix = * + nix)

* Bao gồm cả Unix gốc, BSD, Linux, macOS,... và các hệ điều hành tuân theo chuẩn POSIX.


### macOS thuộc loại nào?

#### Khái niệm về macOS

* macOS là hệ điều hành dành cho máy tính Apple (MacBook, iMac,...)

#### macOS thuộc loại nào?

macOS không phải là Unix gốc, nhưng:

* Nó dựa trên BSD + Mach Kernel.

* Nó đạt chứng chỉ UNIX của The Open Group -> tức là macOS là một hệ điều hành "chuẩn Unix".

Như vậy, về lịch sử, nó là Unix-like (giống Unix, vì kế thừa BSD), còn theo tiêu chuẩn hiện tại là Unix chính thức.

## Alpine và Ubuntu?

### Alpine

#### Khái niệm:

Alpine Linux là một bản phân phối Linux hướng đến sự tối giản, cả về không gian và phạm vi, cũng như tính bảo mật cao hơn.

#### Đặc điểm:

* Alpine Linux sử dụng một kỹ thuật được gọi là các tệp thực thi độc lập với vị trí (position-independent executables) để ngẫu nhiên hóa vị trí của các chương trình trong bộ nhớ. Điều này khiến kẻ tấn công khó khai thác các lỗ hổng trong bộ nhớ và chiếm quyền kiểm soát máy.

* Bản phân phối cũng có cấu hình tối giản. Nó có kích thước nhỏ do sử dụng bộ BusyBox để cung cấp hầu hết các tiện ích trong một tệp thực thi.

* Kích thước nhỏ của Alpine khiến nó phù hợp với những người dùng container, đặc biệt là Docker.

### Ubuntu

#### Khái niệm:

Ubuntu là hệ điều hành mã nguồn mở dựa trên Linux. Nó mang lại các ưu điểm cốt lõi như tính ổn định, bảo mật và độ tin cậy cao của hệ điều hành mã nguồn mở.

#### Đặc điểm:

* Ubuntu có mã nguồn mở, có nghĩa là bất kỳ ai cũng có thể xem, sửa đổi, và phân phối lại mã nguồn của nó.

* Ubuntu được thiết kế để dễ sử dụng, ngay cả với những người không có kinh nghiệm nhiều về Linux. 

* Ubuntu đi kèm với một loạt phần mềm sẵn có, bao gồm trình duyệt web, bộ xử lý văn bản, bảng tính, trình chiếu, trình chỉnh sửa ảnh, và nhiều hơn nữa. Nó cũng hỗ trợ việc cài đặt thêm phần mềm từ các kho lưu trữ phần mềm của nó.

* Ubuntu được xem là một hệ điều hành an toàn và đáng tin cậy, với các cập nhật bảo mật thường xuyên.

## VNC?

#### Khái niệm:

* VNC là viết tắt của *Virtual Network Computing*.

* Là một hệ thống chia sẻ màn hình đồ họa sử dụng giao thức Remote Frame Buffer (RFB) để điều khiển máy tính từ xa.

* Theo mô hình client-server: một máy tính sẽ đóng vai trò server (máy chủ) chia sẻ màn hình, bàn phím, chuột; máy khác đóng vai trò client/viewer (máy khách) nhận màn hình và gửi lệnh nhập (chuột, bàn phím) về.

#### Thành phần

* VNC Server: phần mềm trên máy muốn được điều khiển từ xa, chịu trách nhiệm:

    * Chia sẻ màn hình (framebuffer) lên mạng.

    * Nhận tín hiệu chuột / bàn phím từ phía client. 


* VNC Client / Viewer: phần mềm trên máy người điều khiển, dùng để xem màn hình máy server, gửi các tương tác của người dùng (mouse, keyboard) về server. 

* Giao thức RFB: Remote FrameBuffer Protocol, giao thức chính để trao đổi hình ảnh màn hình (framebuffer) và các sự kiện đầu vào. 

#### Cách hoạt động

Máy chủ (server) lấy “framebuffer” — tức là dữ liệu ảnh đại diện cho màn hình hiện tại tại thời điểm đó. 

Khi có sự kiện, ví dụ con trỏ chuột di chuyển, bàn phím nhập liệu từ client, client gửi các sự kiện này qua mạng đến server; server cập nhật màn hình dựa vào sự kiện đó và gửi hình ảnh mới lại client. 

Thường dùng cổng TCP 5900 + N (với N là số màn hình / phiên), một số triển khai hỗ trợ qua trình duyệt hoặc qua HTTP/Java applet. 

#### Đặc điểm

* Đa nền tảng: Có server/client cho rất nhiều hệ điều hành như Windows, Linux, macOS.

* Không phụ thuộc vào OS cụ thể — client với server có thể khác hệ điều hành vẫn kết nối được nếu hỗ trợ RFB.

* Truy cập từ xa & điều khiển đầy đủ: người dùng có thể xem màn hình, điều khiển chuột/bàn phím từ xa như đang ngồi tại máy server.

* Ứng dụng linh hoạt: hỗ trợ kỹ thuật từ xa, quản trị hệ thống, làm việc từ xa, đào tạo, hỗ trợ máy tính cá nhân ở nhà v.v.





