Họ Tên: Chu Văn Chung
Mã SV: 1151225301
Dự Án: Hệ Thống Quản Lý Nhiệt Độ Thông Minh
Mô Tả
Dự án này sẽ tạo ra một hệ thống giám sát và quản lý nhiệt độ trong các phòng của một tòa nhà. Các cảm biến nhiệt độ sẽ gửi dữ liệu đến Node-RED, sau đó dữ liệu này sẽ được lưu trữ vào SQL Server và có thể được truy xuất và hiển thị qua một API được xây dựng bằng Python FastAPI.

Các Thành Phần Chính
Cảm Biến Nhiệt Độ (Giả Lập):

Sử dụng một cảm biến giả lập để gửi dữ liệu nhiệt độ định kỳ đến Node-RED.
Node-RED:

Nhận dữ liệu từ cảm biến.
Xử lý và chuyển tiếp dữ liệu đến SQL Server.
Tạo các luồng xử lý để gửi cảnh báo nếu nhiệt độ vượt quá ngưỡng cho phép.
SQL Server:

Lưu trữ dữ liệu nhiệt độ nhận được từ Node-RED.
Lưu trữ thông tin các phòng và các ngưỡng nhiệt độ cho phép.
Python FastAPI:

Xây dựng API để truy xuất dữ liệu nhiệt độ từ SQL Server.
Cung cấp endpoint để cập nhật ngưỡng nhiệt độ cho phép của các phòng.
Cung cấp endpoint để lấy dữ liệu lịch sử nhiệt độ.
Giao Diện Người Dùng (Optional):

Một giao diện web đơn giản để hiển thị dữ liệu nhiệt độ theo thời gian thực và cài đặt ngưỡng nhiệt độ.
Các Bước Triển Khai
1. Thiết Lập Node-RED
Cài đặt Node-RED.
Tạo luồng để nhận dữ liệu từ cảm biến (có thể sử dụng node inject để giả lập dữ liệu).
Sử dụng node mssql để gửi dữ liệu đến SQL Server.
2. Cấu Hình SQL Server
Tạo các bảng cần thiết: Rooms, TemperatureReadings, Thresholds.
Thiết lập kết nối từ Node-RED đến SQL Server.
3. Phát Triển FastAPI
Cài đặt FastAPI và các thư viện cần thiết (fastapi, pydantic, sqlalchemy).
Xây dựng các endpoint:
GET /temperatures: Lấy dữ liệu nhiệt độ hiện tại.
GET /temperatures/history: Lấy dữ liệu lịch sử nhiệt độ.
POST /thresholds: Cập nhật ngưỡng nhiệt độ cho phép.
Kết nối FastAPI với SQL Server sử dụng SQLAlchemy hoặc các thư viện tương tự.
4. (Optional) Xây Dựng Giao Diện Người Dùng
Sử dụng HTML/CSS/JavaScript để xây dựng giao diện đơn giản.
Hiển thị dữ liệu nhiệt độ theo thời gian thực (sử dụng thư viện như Chart.js).
Tạo form để cập nhật ngưỡng nhiệt độ.
