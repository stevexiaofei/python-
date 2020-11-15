# python服务

## 通过http服务将当前文件开放访问

```python
python -m http.server 9999
```

python建立ftp服务

```python
from pyftpdlib.authorizers import DummyAuthorizer 
from pyftpdlib.handlers import FTPHandler 
from pyftpdlib.servers import FTPServer 
authorizer = DummyAuthorizer() 
authorizer.add_user("user", "12345", "/home/bob", perm="elradfmw") 
authorizer.add_anonymous("/home/bob") 
handler = FTPHandler 
handler.authorizer = authorizer 
server = FTPServer(("10.227.77.17", 23), handler) 
server.serve_forever()
```



