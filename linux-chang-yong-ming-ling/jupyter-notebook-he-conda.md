# jupyter notebook和conda

## pip python的包管理器 

python第三方python的安装 

```text
pip install xxx
或者指定版本
pip install xxx>=1.xx.0
```

pip install 默认会从国外的官方库下载，速度较慢，国内的镜像源要快很多。国内的镜像有

| 名称 | URL |
| :--- | :--- |
| 阿里云 | [http://mirrors.aliyun.com/pypi/simple/ ](http://mirrors.aliyun.com/pypi/simple/
) |
| 中国科技大学 | [https://pypi.mirrors.ustc.edu.cn/simple/ ](https://pypi.mirrors.ustc.edu.cn/simple/
) |
| 豆瓣\(douban\) | [http://pypi.douban.com/simple/ ](http://pypi.douban.com/simple/
) |
| 清华大学 | [https://pypi.tuna.tsinghua.edu.cn/simple/ ](https://pypi.tuna.tsinghua.edu.cn/simple/
) |

安装时可以用如下命令：

```text
pip install numpy -i https://pypi.tuna.tsinghua.edu.cn/simple
```

也可以将pip源写入到文件中，~/.pip/pip.conf

```c
 [global]
 index-url = https://pypi.tuna.tsinghua.edu.cn/simple
```

## conda相关的常用命令



