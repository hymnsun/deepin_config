# deepin v20体验

```python {.line-numbers,cmd}
print("hello,deepin v20")
```

## 0 设置
- 讯飞输入法，英文键盘,安装后可能需要重启输入法
- 系统字体为Noto Serif CJK JP
- chrome，QQ，wechat，网易云音乐，xmind，wps
- vscode 中文模式下鼠标左键不能拖选
- pdf:`sudo apt install evince`


## [1 常用软件](./workware_conf.md)
- anaconda
- Pycharm
- V2Ray
- Texlive2020
- VScode


## [2 LINUX 指令](./linux.md)
- 常用
- [shell](./shell.md)
- web服务器
    - [Hexo](https://blog.csdn.net/qq_40311985/article/details/107159107)
    - [WordPress](./woedpress)
    - python + django
- 文件服务器

## 3 Docker配置

## [4 Git管理](https://blog.csdn.net/qq_40311985/article/details/107158908)
- git 连接github：
    ```
    ssh-keygen -t rsa -C "XXXXXXXXX@163.com"
    key dir：/home/hymnsun/.ssh/id_rsa
    ```
-------
## BUG
- [x] 无法安装texstudio for linux 导致系统锁死
    >  sudo apt --fix-broken install
- [ ] texlive 无法更新包，直接安装tex live --full


## what to do
- [x] 梯子
- [ ] 下载
- [ ] web + 文件服务器 + 负载均衡
- [x] 系统备份
    - `df -h`查看有无其它系统盘挂在在`media`分区，有则`umount`
    - `sudo tar cvpzf backup.tgz --exclude=/proc --exclude=/lost+found --exclude=/backup.tgz --exclude=/mnt --exclude=/sys /`
    - `sudo tar xvpfz backup.tgz -C /`
    - `mkdir /proc && mkdir /lost+found && mkdir /sys && mkdir /mntls`