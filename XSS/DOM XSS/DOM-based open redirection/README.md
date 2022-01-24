**Yêu cầu: Đây là lỗi open-redirection (chuyển hướng), để solved thì ta sẽ khai thác và chuyển hướng người dùng tới máy chủ exploit**
![image](https://user-images.githubusercontent.com/62832067/150770691-70197397-2b85-4e57-bea5-995861d4ae10.png)
Source code chứa 1 đoạn mã có chức năng quay về home khi đang ở trong 1 bài viết
``` php
<a href='#' onclick='returnURL' = /url=https?:\/\/.+)/.exec(location);
   if(returnUrl)location.href = returnUrl[1];
   else location.href = "/"'>Back to Blog</a>
```
<br> Hàm ```onlick``` có chức năng lấy địa chỉ của bài viết match với regex ```/url=(https?:\/\/.+)/```  để tạo ra một mảng, nếu mảng này tồn tại,ta click vào thẻ a, 
giá trị của url sẽ là phần tử ```returnUrl[1]``` 
<br> Vì thế để chuyển tới url của exploit server, ta có thể thêm 1 tham số url trên thanh địa chỉ của 1 bài viết là link của exploit server tương ứng với phần tử ```returnUrl[1]```: 
```https://ac231f3c1e159555c06f5109004e001c.web-security-academy.net/post?postId=7&url=https://exploit-acff1f4a1e8d95c4c03151c4019f0035.web-security-academy.net/```
