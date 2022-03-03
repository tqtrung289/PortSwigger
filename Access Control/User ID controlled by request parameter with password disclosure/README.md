Yêu cầu: ID người dùng được kiểm soát bằng request param nhưng bị lộ mật khẩu.
<br> Đây là lỗi IDOR (Insecure direct object references - Tham chiếu đối tượng trực tiếp không an toàn). 
IDOR phát sinh khi một ứng dụng sử dụng đầu vào do người dùng cung cấp để truy cập trực tiếp vào các đối tượng 
và kẻ tấn công có thể sửa đổi đầu vào để có được quyền truy cập trái phép. Ở đây là ta có thể sửa param trực tiếp trên URL

<br> Sau khi đăng nhập bằng tk wiener ta có thể thấy trên url có param của id, ta sửa thành administrator để vào được account admin
![image](https://user-images.githubusercontent.com/62832067/156543521-04fb69c7-d82e-42eb-999a-3a977456b69c.png)
<br> Sau đó ta thấy mật khẩu của tk admin, ta chỉ cần sửa thuộc tính ```type``` của mk thành ```test``` là có thể thấy mk của tk admin dưới dạng chữ
![image](https://user-images.githubusercontent.com/62832067/156543755-0fea164c-5ff1-4f26-aa38-95b08bc0f7b1.png)

<br> Sử dụng mk này để đăng nhập rồi xoá user carlos để hoàn thành
![image](https://user-images.githubusercontent.com/62832067/156543764-fd7e380d-4df4-4847-8b36-ae6afccfeeb4.png)
