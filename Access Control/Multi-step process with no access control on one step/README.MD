Yêu cầu: Exploit các lỗ hổng của Admin Panel để nâng role lên admin cho tk user
<br> Bài này có lỗi ở các bước quá trình xác thực nâng role, khi không cần kiểm tra đó có phải seesion của tk admin không 

<br> Trước tiên, ta đăng nhập tài khoản admin đề bài cho, thực hiện nâng role cho tài khoản carlos để bắt request. Ở đây ta lưu ý tới dòng param dưới cùng, sau khi ấn upgrade sẽ có 1 bước xác thực Yes/No. 
![image](https://user-images.githubusercontent.com/62832067/156527758-d1fa72d0-c033-4497-8218-93e545604bb0.png)
![image](https://user-images.githubusercontent.com/62832067/156528219-b15c7060-5c4a-4f8c-bf7f-0e5be56028c8.png)

<br> Dòng param cần lưu ý ở đây là 
```action=upgrade&confirmed=true&username=carlos```

<br> Ta send request này sang Repeater để thay đổi, tiếp đến ta đăng nhập tk wiener để lấy seesion của tk này. Thay thế seesion và sửa param thành ``` action=upgrade&confirmed=true&username=wiener``` và ta đã nâng role thành công
![image](https://user-images.githubusercontent.com/62832067/156528433-63df830c-6594-420c-912f-05143b5bd664.png)
![image](https://user-images.githubusercontent.com/62832067/156528528-b7947444-c5e8-4126-ae48-6822b614f2dc.png)

