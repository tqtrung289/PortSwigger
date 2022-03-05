Yêu cầu: Brute Force tiếp tục. Nhận diện username đúng qua lỗi logic của việc khoá tài khoản
<br> Ta thực hiện brute force username cùng với password là ```null``` và tìm được user ```app1``` có length response khác với phần còn lại
<br> Ở đây ta sử dụng tính năng ClusterBomb để tấn công. Khác với Pitchfork là sẽ kết hợp từng cặp giá trị của mỗi payload và số request là số giá trị của payload nhỏ hơn, ClusterBomb sẽ thử tất cả giá trị của payload 1 với payload 2 
<br> Ví dụ:
<br> Payload 1: 100, Payload 2 200 => PitchFork sẽ có 100 request còn ClusterBomb có 100x200=20000 request
![image](https://user-images.githubusercontent.com/62832067/156864510-11b74ddb-1f21-487e-ad89-cb845e52914d.png)
<br> Tiếp đó ta brute wordlist password và thấy password ```klaster``` không có string trả về như các pass khác
![image](https://user-images.githubusercontent.com/62832067/156864627-601e0352-e0b5-4020-8a8c-5386011c9603.png)
![image](https://user-images.githubusercontent.com/62832067/156864669-1f776379-7658-462e-ab40-32fc1ec6daec.png)
