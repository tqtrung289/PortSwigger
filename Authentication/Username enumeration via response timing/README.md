Yêu cầu: Vẫn là brute force Username + Password
<br> Bài này có phần khó hơn đó là sẽ có limit IP đăng nhập, tuy nhiên ta có thể bypass bằng cách thêm vào header của request: ```X-Forwarded-For: [x]```
<br> X-Forwarded-For: Có thể hiểu đơn giản là một phương pháp để xác định địa chỉ IP gốc của máy khách kết nối với máy chủ web và ta sẽ thay đổi giá trị [x] để thay đổi IP kết nối tới server
