Yêu cầu: Tương tự bài Method Base
<br> Đăng nhập tk admin và upgrade user carlos để lấy mẫu request
![image](https://user-images.githubusercontent.com/62832067/156730366-68ef749e-fb76-4b28-a883-c758a7a724ea.png)

<br> Sau đó đăng nhập tk wiener để lấy seesion 
![image](https://user-images.githubusercontent.com/62832067/156730963-4965de73-ed56-4af8-a4f0-4cdd84ef3255.png)

<br> Thay thế username và seesion sau đó send request, Burp báo 302 Found tức là tìm thấy chuyển hướng, ```Follow Redirection``` rồi F5 là ta thấy user wiener đã thành admin
![image](https://user-images.githubusercontent.com/62832067/156731175-05e3491b-2862-4e49-971f-90e3373ce8ea.png)
![image](https://user-images.githubusercontent.com/62832067/156731432-665440b3-29bd-4f49-b3b0-acfbac3c270f.png)
