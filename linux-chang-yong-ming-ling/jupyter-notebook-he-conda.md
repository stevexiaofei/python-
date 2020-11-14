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

* _**conda list 查看安装了那些包**_
* _**conda env list 或 conda info -e 查看当前存在哪些虚拟环境**_
* _**conda update conda 检查更新当前conda**_
* _**conda create -n your\_env\_name python=X.X 新建conda环境**_
* _**conda remove -n env\_name --all**_

## jupyter notebook\([参考链接](https://juejin.im/post/6844903842497167374)\)

### 带参数启动jupyter notebook

```c
jupyter notebook --no-browser --port 6000 --ip=202.121.181.3
```

### 修改jupyter notebook的启动配置文件

1. `jupyter notebook --generate-config` 生成的配置文件在~/.jupyter/jupyter\_notebook\_config.py
2. 设置密码  ****`jupyter notebook password`
3. 修改文件

```c
vim ~/.jupyter/jupyter_notebook_config.py
c.NotebookApp.ip = '*' # 开启所有的IP访问，即可使用远程访问
c.NotebookApp.open_browser = False # 关闭启动后的自动开启浏览器
c.NotebookApp.port = 8888  # 设置端口8888，也可用其他的，比如1080，8080等等
c.NotebookApp.notebook_dir = '指定的工作路径'”可以改变jupyter开始运行时的工作目录
```

### jupyter kernel的操作

* 移除kernel `jupyter kernelspec remove python3`
* 添加kernel 的方法`python -m ipykernel install –user --name XXXX`
* 查看kernel `jupyter kernelspec list`
* [matlab kernel的安装](https://www.zhihu.com/question/65744778)





