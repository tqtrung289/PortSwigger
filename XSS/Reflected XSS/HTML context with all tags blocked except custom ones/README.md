Ở đây các tag HTML đều bị chặn, vì thế ta sử dụng custom tag trong phần exploir server: **/?search=<xss+id=x+onfocus=alert(document.cookie)+tabindex=1>#x**
![image](https://user-images.githubusercontent.com/62832067/150635093-326fd7ef-1dca-442e-bb30-a9068ac8c4a0.png)
<br> Alert hiện ra thành công 
![image](https://user-images.githubusercontent.com/62832067/150635102-9d583335-1e4a-43b7-bc58-4e9040ab68bf.png)
<br> Check log ta thấy hành vi có gọi API document.cookie vừa rồi đã gọi ra Cookie của "User-Agent"
![image](https://user-images.githubusercontent.com/62832067/150635168-1fa2483a-ebaf-49a8-88ff-d538764ffc9b.png)


