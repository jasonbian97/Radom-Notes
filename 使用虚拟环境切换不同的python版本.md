# 使用虚拟环境切换不同的python版本

安装了virtualenv和virtualenvwrapper，

```
mkvirtualenv -p /full/path/of/your/executable/python envname
```

虚拟环境被放在了~/.virtualenvs文件夹下，使用

```
workon
```

切换不同版本的虚拟环境

使用

```
rmvirtualenv envname
```

删除某一个虚拟工作环境

进入虚拟环境后，使用

```
$python
$which python
```

可以观察interpreter所在的位置和所使用python的版本

PS： 在pycharm—settings—interpreter—中可以选择已有的虚拟环境，似乎也可以创建新的virtualenv

## 解决pip install 很慢的问题

使用清华镜像，不会被墙，速度会有很大提升：

```
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple torch
```

## 在新建的虚拟环境中安装包

首先希望transfer的虚拟环境中使用

```
pip freeze > requirement.txt
```

然后将这个txt复制到./virtulaenv/newenv下

然后workon newenv

然后使用

```
pip install -i https://pypi.tuna.tsinghua.edu.cn/simple -r requrement.txt 
```

