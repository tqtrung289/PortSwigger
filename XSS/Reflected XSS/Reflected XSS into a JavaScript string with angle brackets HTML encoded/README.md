Yêu cầu lab là làm sao để *breaks out of the JavaScript string* để gọi được alert lên 
<br> Ta nhập thử 'test' vào ô tìm kiếm để xem cách xử lý của trang web. Trong thẻ Script ta thấy biến searchTerm được khai báo là **searchTerms = 'test';** để bypass đoạn này 
ta sẽ tìm kiếm bằng cú pháp **test'; alert() //**
![image](https://user-images.githubusercontent.com/62832067/150641988-2811a2c1-27f7-444e-9fa2-db30e814abdd.png)
<br> Kết quả ta có được truy vấn sẽ thành 1 câu lệnh đầy đủ như hình:
<br> Giải thích **test';** để kết thúc lệnh khai báo biến rồi sau đó chạy **alert()**, dùng **//** để comment đoạn **';** thừa ở phía sau
![image](https://user-images.githubusercontent.com/62832067/150642248-ebb2e4d0-910c-4ffa-abd4-907d428bcd2e.png)
