Yêu cầu: Brute Cookie để đăng nhập vào user carlos bởi lab cho phép người dùng tiếp tục đăng nhập ngay cả khi đóng session
<br> Trước tiên ta đăng nhập user wiener để bắt được request có chứa cookie
<br> Decode cookie base64 ta được nội dung cookie bao gồm ```wiener:``` đoạn sau dấu ```:``` là 1 đoạn hash, do chưa biết hash gì nên ta có thể mò tay và kết quả là MD5 
<br> Hoặc cách khác là sử dụng tool <a href="crackstation.net">crackstation.net</a> để phát hiện loại mã hash 
<br> Password được mã hoá MD5 và chèn vào cookie. Do đã có form Cookie ta bắt đầu brute
