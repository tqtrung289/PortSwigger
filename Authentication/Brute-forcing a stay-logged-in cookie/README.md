Yêu cầu: Brute Cookie để đăng nhập vào user carlos bởi lab cho phép người dùng tiếp tục đăng nhập ngay cả khi đóng session
<br> Trước tiên ta đăng nhập user wiener và chọn ```Stay logged in``` để bắt được request có chứa cookie
![image](https://user-images.githubusercontent.com/62832067/156865900-f35e9c4f-369f-45a1-b5d5-0cc974fca636.png)

<br> Decode cookie base64 ta được nội dung cookie bao gồm ```wiener:...``` đoạn sau dấu ```:``` là 1 đoạn hash, do chưa biết hash gì nên ta có thể mò tay và kết quả là MD5
<br> Hoặc cách khác là sử dụng tool <a href="crackstation.net">crackstation.net</a> để phát hiện các loại mã hash thông dụng
![image](https://user-images.githubusercontent.com/62832067/156865914-1e60dfa7-cfd8-490d-853a-5e9091848c38.png)
![image](https://user-images.githubusercontent.com/62832067/156865957-b98a2b85-7a33-43b6-ad3b-5739a84eb3d0.png)

<br> Cookie gốc có dạng: ```wiener:peter``` 
<br> Password được mã hoá MD5 và chèn vào cookie rồi sau đó mã hoá B64. Do đã có form Cookie ta bắt đầu brute wordlist password và với các rule như sau
![image](https://user-images.githubusercontent.com/62832067/156866028-a6b7519c-c6ce-4b8a-8dbf-41beff6a5abc.png)
GrepMatch add "Update email" là bởi vì khi ta đăng nhập thành công sẽ có string này
![image](https://user-images.githubusercontent.com/62832067/156866474-46a0892a-28a7-47c4-b465-7a5eb51a77f3.png)
![image](https://user-images.githubusercontent.com/62832067/156866457-d7f1374a-0945-4744-8f43-54b7fe818150.png)
