Yêu cầu: Bài này có lỗ hổng bảo mật theo chiều ngang, xác định người dùng bằng GUID. Ta cần tìm GUID của tk carlos và submit API key tương ứng
Trong 1 số ứng dụng, param khó có thể dự đoán được do trang web sử dụng 1 mã định danh duy nhất cho 1 user (Globally Unique Identifiers/GUID) thay vì sử dụng số thứ tự tăng dần do đó kẻ tấn công khó có thể đoán được mã định danh các user khác. Tuy nhiên GUID có thể bị lộ ở những nơi khác chẳng hạn như ở phần bình luận, đánh giá, hay ở bài này là ở url của Blog.

<br> Ta vào 1 blog bất kì có auth là carlor, dựa vào url ta lấy được GUID 
```userId=1656d4f9-19e9-45e9-9f8e-f6c79daefb91```
![image](https://user-images.githubusercontent.com/62832067/156533159-822d1a5d-5e04-4977-8d6a-bcf136218fab.png)

<br> Ta đăng nhập vào user wiener của bài cho để lấy được request, sau đó sửa GUID như GUID ta lấy được ở trên (sửa dòng số 1) rồi resend để có được API key của tk carlos
<br>
![image](https://user-images.githubusercontent.com/62832067/156533783-90039e67-aa5e-48f4-b260-47325dc7201e.png)
![image](https://user-images.githubusercontent.com/62832067/156534087-e44c9087-786f-4022-b999-d193bc8c674f.png)
