# Giám sát hiệu suất Server Linux/Windows về thông số : RAM, CPU, DISK
NỘI DUNG
I.	Giới thiệu về phần mềm Zabbix.
1.	Sơ lược về Zabbix.
Zabbix được thành lập vào năm 1998. Đây là dự án công ty của Alexei Vladishev. Khi đó, ông đang là nhân viên quản trị hệ thống trong một ngân hàng chịu trách nhiệm quản lý cơ sở dữ liệu. Để tự động hóa công việc thường ngày, ông Vladishev đã tạo ra một nguyên mẫu đầu tiên của Zabbix. 
Zabbix là một công cụ mã nguồn mở nổi tiếng giải quyết cho ta các vấn đề về giám sát – là phần mềm sử dụng các tham số của một mạng, tình trạng và tính toàn vẹn của Server cũng như các thiết bị mạng.
Với cơ chế thông báo linh hoạt, người dùng có thể cấu hình cảnh báo qua email cho mọi sự kiện, giúp phản ứng nhanh với sự cố host. Tất cả báo cáo, thống kê và cấu hình của Zabbix đều được truy cập qua giao diện người dùng web. Giao diện này cho phép đánh giá trạng thái mạng và host từ bất kỳ địa điểm nào. Zabbix là một phần mềm miễn phí, phát hành theo GPL-General Public License version 2.
2.	Các thành phần cơ bản của Zabbix.
2.1.	Zabbix Server
Đây là ứng dụng chương trình dịch vụ chính của dịch vụ Zabbix. Zabbix Server sẽ chịu trách nhiệm cho các hoạt động kiểm tra dịch vụ mạng từ xa, thu thập thông tin, lưu trữ, hiển thị, cảnh báo,… từ đó các quản trị viên có thể thao tác giám sát hệ thống tốt nhất.
 

2.2.	Zabbix Proxy
Là phần tùy chọn của Zabbix. Nó có nhiệm vụ thu nhận dữ liệu, lưu trong bộ nhớ đệm và chuyển đến Zabbix Server. Zabbix Proxy là một giải pháp lý tưởng cho việc giám sát tập trung của các địa điểm từ xa, chi nhánh công ty, các mạng lưới không có quản trị viên nội bộ.
2.3.	Zabbix Agent 
Để giám sát chủ động các thiết bị cục bộ và các ứng dụng (ổ cứng, bộ nhớ, …) trên hệ thống mạng. Zabbix Agent sẽ được cài lên trên Server và từ đó Agent sẽ thu thập thông tin hoạt động từ Server mà nó đang chạy và báo cáo dữ liệu này đến Zabbix Server để xử lý.
2.4.	Giao diện web
Để dễ dàng truy cập dữ liệu theo dõi và sau đó cấu hình từ giao diện web cung cấp. Giao diện là một phần của Zabbix Server, và thường chạy trên các máy chủ.
3.	Những tính năng cơ bản của Zabbix.
Zabbix cho phép người dùng giám sát các thiết bị trong mạng, bao gồm các router, switch, firewall và các thiết bị khác. Nó cũng hỗ trợ giám sát các giao thức như SNMP, TCP, UDP ,...
Zabbix có khả năng giám sát được các thông tin liên quan tới các thiết bị mạng như băng thông, CPU, bộ nhớ và tài nguyên khác.
Zabbix hỗ trợ kiểm tra kết nối đến các thiết bị mạng và kiểm tra trạng thái từ xa của các máy tính và các thiết bị khác.
Zabbix giám sát các kết nối TCP/UDP và cung cấp các thông tin về tình trạng của chúng.
Zabbix giám sát các trang web, đánh giá hiệu suất tải trang để giúp xác định các vấn đề và phát hiện sự cố.
4.	Ưu và nhược điểm của Zabbix.
4.1.	Ưu điểm
•	Hỗ trợ giám sát đa nền tảng: Có thể giám sát hệ thống trên nhiều nền tảng khác nhau, bao gồm Linux, Windows, Unix và các thiết bị khác.
•	Giao diện web đẹp mắt, thân thiện người dùng.
•	Thông báo sự cố qua email và SMS.
•	Mã nguồn mở và chi phí thấp.
4.2.	Nhược điểm
•	Không có giao diện web mobile hỗ trợ.
•	Không phù hợp với hệ thống mạng lớn, nhiều thiết bị client cần giám sát. Lúc này phát sinh vấn đề hiệu suất về PHP và Database, ...
•	Thiết kế template/alerting rule đôi khi khá phức tạp đối với người mới bắt đầu.
•	Cộng đồng nhỏ hơn: Mặc dù Zabbix có một cộng đồng người dùng tích cực, nhưng nó vẫn nhỏ hơn so với một số công cụ mã nguồn mở phổ biến khác.
•	Ít tài nguyên học tập: Có ít khóa học trực tuyến và tài liệu hướng dẫn từ bên thứ ba so với các công cụ giám sát phổ biến khác.
