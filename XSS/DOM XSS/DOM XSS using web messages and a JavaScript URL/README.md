**Yêu cầu: Tạo 1 page HTML trên máy chủ exploit để gọi được hàm print()/alert()**
<br> Source code bài này cũng có hàm addEventListener(), có phần check hợp lệ url dưới dạng string ở bất kì nơi nào trong message, nếu có url thì chuyển tới trang đó 
![image](https://user-images.githubusercontent.com/62832067/150760493-3fd3ad3f-ae47-4cd9-9116-aaf0fe9820a7.png)
<br> Vì thế ta tiếp tục sử dụng **postMessage()** với điều kiện message có chứa http: hoặc https: và chèn thêm script bên trong payload: 
![image](https://user-images.githubusercontent.com/62832067/150761510-38cfaf76-19be-4f50-a4f7-87c5d74f4ad3.png)

