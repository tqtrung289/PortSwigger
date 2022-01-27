Yêu cầu: Vào được Admin panel và xoá tài khoản carlos
<br> Khi ta vào admin panel ta thấy có 1 request GET /admin và ta đoán được có thể truyền được param này vào url để có khả năng truy cập admin panel
![image](https://user-images.githubusercontent.com/62832067/151326527-40bf1d80-6f57-46b3-a9e9-f80b35d987b7.png)
Theo gợi ý của bài ta sẽ sử dụng headers **X-Original-URL** để có thể chèn /admin vào url gốc [URL rewrite vulnerability](https://www.acunetix.com/vulnerabilities/web/url-rewrite-vulnerability/) 
<br> Và ta đã vào được trang admin thành công.
![image](https://user-images.githubusercontent.com/62832067/151326532-e229fe9a-d88c-4bc8-8cdd-d16d8ba4c697.png)
<br> Để xoá user carlos ta truyền vào param **?username=carlos** khi đã ở trong path **/admin/delete** (Làm theo gợi ý nên chỗ này chưa biết giải thích tại sao)
![image](https://user-images.githubusercontent.com/62832067/151326696-7b7aa5c6-7ddc-4d17-b463-8df5ac29951c.png)
