# mmcv
#### 官方文档
https://mmdetection.readthedocs.io/zh_CN/stable/tutorials
#### config配置文件说明
查看官方文档即可，注意在进行配置文件继承的时候：<br/>
config_a.py
```
filename = ‘/mnt/wangyi’
b = dict(a = filename)
```

config_b.py
```
_base_ = ['./config_a.py’]
此时如果需要修改b[a]则需要按照下述方法进行操作：
filename = ‘/mnt/mgtv’
b = dict(a = filename)
仅仅修改filename是不能修改变量b的值的
```