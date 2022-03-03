
Đầu tiên, ta đăng nhập bằng tk admin, promote user carlos lên admin để lấy được request
![image](https://user-images.githubusercontent.com/62832067/156549887-53ccee0f-ea9d-4a8f-8e6d-8901a1aabf93.png)

<br> Sau đó ta đăng nhập user wiener để lấy seesion, thay seesion đó vào request trên và thử resend, response báo lỗi "Unauthorized"
![image](https://user-images.githubusercontent.com/62832067/156550008-eb9bd2e3-b274-4c66-a934-f821514817cf.png)

<br> Đổi phương thức từ ```POST``` sang ```POSTX``` ta nhận được response báo thiếu param username
![image](https://user-images.githubusercontent.com/62832067/156550171-014a9540-b06a-4485-ae74-1dc6568495b5.png)

<br> Để có được param username ta cần chuyển request từ dạng post thành get, thay thế seesion là seesion của tk wiener rồi sau đó forward là thành công 
![image](https://user-images.githubusercontent.com/62832067/156554347-a9bef33a-a3a4-47b6-926b-92313ac6d0ce.png)
![image](https://user-images.githubusercontent.com/62832067/156554350-222e6470-1ffc-42de-a9c9-1bbea08401f7.png)
