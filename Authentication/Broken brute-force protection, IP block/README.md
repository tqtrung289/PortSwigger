Yêu cầu: Brute Force. Tuy nhiên khi quá 3 lần sai pass, ip sẽ bị ban. Để bypass thì sẽ nhập account đúng trước khi bị ban. 
![image](https://user-images.githubusercontent.com/62832067/156862195-5b2e9f03-a5b7-432c-b379-98dc0ff0b93f.png)
<br> Ta tạo 2 wordlist tương ứng: Cứ dòng lẻ thì là account "wiener" đúng còn dòng chẵn là account brute 
```
password = 'pass.txt' 
add = open("pass2.txt","w")
with open(password) as pwd:
    line = pwd.readline()
    while line:
        add.write("peter\n")
        add.write(line.strip())
        add.write("\n")
        line=pwd.readline()
add.close()
```
![image](https://user-images.githubusercontent.com/62832067/156863679-df8fcf98-2959-482a-a62a-ca27ecb3b61b.png)

Chỉnh resource pool tách từng request riêng
![image](https://user-images.githubusercontent.com/62832067/156877798-a8de940a-ef77-4ea2-b0a7-81057a03bb2f.png)
![image](https://user-images.githubusercontent.com/62832067/156877674-c6cd444b-4a81-4276-971c-7654a2e0895b.png)
