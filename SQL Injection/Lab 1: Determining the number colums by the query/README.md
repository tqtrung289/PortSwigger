Có 2 cách để xác định số cột của 1 DB: 
<br>**Cách 1: Sử dụng truy vấn Order by: 'ORDER BY (n)--**
<br>Truy vấn Order by trong SQL sẽ sắp xếp các giá trị kết quả của số thứ tự cột ta truyền vào, ở đây ta sẽ thử các param với số cột tăng dần 1,2,3,4,...,n cho tới khi server trả về lỗi ở số thứ n từ đó ta sẽ xác định được số cột là n-1
<br> Ở đây số cột là 3 vì khi đổi thành 4 kết quả trả về báo lỗi
![image](https://user-images.githubusercontent.com/62832067/150272482-9ddd9e82-01e2-4265-91f2-3c8517c2d944.png)
![image](https://user-images.githubusercontent.com/62832067/150272624-d74fe2da-fe0f-40c2-9730-1af1baa56df7.png)
<br>
<br>
**Cách 2: Sử dụng truy vấn Union Select: 'UNION SELECT NULL,NULL,NULL--**
<br>Mỗi lệnh SELECT trong toán tử UNION phải có cùng số cột trong bộ kết quả với kiểu dữ liệu tương ứng. Vì thế khi ta truyền vào 3 trường dữ liệu tương ứng là NULL,NULL,NULL trùng với 3 cột của DB ta sẽ nhận đuọc kết quả trả về hợp lệ, ngược lại sẽ nhận được kết quả báo lỗi.
![image](https://user-images.githubusercontent.com/62832067/150272899-63d9965d-0088-4dc3-ac51-6365099e3bd4.png)
