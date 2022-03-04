Yêu cầu: Vẫn là brute force Username + Password
<br> Bài này có phần khó hơn đó là sẽ có limit IP đăng nhập, tuy nhiên ta có thể bypass bằng cách thêm vào header của request: ```X-Forwarded-For: [x]```
<br> ```X-Forwarded-For```: Có thể hiểu đơn giản là một phương pháp để xác định địa chỉ IP gốc của máy khách kết nối với máy chủ web và ta sẽ thay đổi giá trị [x] để thay đổi IP kết nối tới server
<br> Để vừa brute IP ([x] tăng dần) vừa brute username + pass thì ta sử dụng chế độ pitchfork để cùng lúc chạy nhiều payload
<br> Ở đây khi brute username ta sẽ để password thật dài để time response khi có username hợp lệ trả về sẽ khác biệt với các username còn lại, và ta tìm được username ```ag```
![image](https://user-images.githubusercontent.com/62832067/156810866-5cd7427f-a246-478a-afcc-640f99fc9ab9.png)
![image](https://user-images.githubusercontent.com/62832067/156810923-9267038a-fb98-421c-bd66-c9ec5dfe838c.png)

<br> Khi đã có username, làm tương tự với password, hợp lệ sẽ trả về status code 302
![image](https://user-images.githubusercontent.com/62832067/156810985-e9b5dddc-f319-4b7c-b6b3-494377678906.png)
![image](https://user-images.githubusercontent.com/62832067/156810143-ec24bef0-15c0-477d-b148-9775407031aa.png)
