Yêu cầu: Brute force username và password theo wordlist nhưng lọc được response theo cách khác

<br> Đầu tiên ta cài đặt response trả về là ```Invalid username or password.``` tuy nhiên khi brute username thì có 1 user được trả về là ```Invalid username or password``` (không có kí tự .)
![image](https://user-images.githubusercontent.com/62832067/156805872-2e57a973-2941-4e41-b7e7-9b2ef46efc98.png)

<br> Tiếp đó ta có được username đúng, ta bruteforce mật khẩu. Và có 1 response trả về báo 302 Found -> Thành công
![image](https://user-images.githubusercontent.com/62832067/156805994-7547db19-5a16-4a0f-8926-542e066c3db9.png)
![image](https://user-images.githubusercontent.com/62832067/156805997-5f6ed29d-11c3-4eda-bc81-23157c63aa79.png)
