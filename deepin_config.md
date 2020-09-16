# deepin v20体验 {ignore}
[TOC]
2020-09-16 停更，修改子文件。
## 设置
- 终端ctrl+C不要修改
- 系统字体为Noto Serif CJK JP

------
## 软件
### 基础软件
- 自带编辑器dedit
- 讯飞输入法，英文键盘和讯飞 切换输入法ctrl+space
- 微信 TIM
- wps
- 迅雷
- 向日葵是
- 网易云音乐
- ~~aria2!~~
    - install aria2:`sudo apt-get install aria2`
    - download aria2 file contain `.conf`,`.log`,`.session` file
    - modify `.conf` file which links to download dir & RPC secret token
    - run aria2 via `aria2c --conf-path='/home/hymnsun/aria2/aria2.conf'`
    - download [AriaNg(front-end)](https://github.com/mayswind/AriaNg/releases) from Github.
    - click `index.html` to fill in RPC secret token in AriaNg settings.
    - download BaidunYun 

`
### [工作软件](./workware_conf.md)


#### chrome
#### vscode
- ctrl+shift+K 删除当前行
- alt+鼠标左键 选中多行
- 插件：MPE
    


--------

## LINUX 指令
    sudo apt-get install [software]
    sudo apt-get remove [software]
    sudo apt-get upgrade 更新已安装包
        
    pwd 显示当前路径
    ls -a 显示所有文件
    ls -la 且显示权限等详细信息
    chmod u+x filename        修改可执行权限
    mkdir <dir_name> 创建目录
    which python


### VIM基本指令
    三种模式：
    查找：
        

### docker的配置

-------------
## Git管理
- git 连接github：
    ```
    ssh-keygen -t rsa -C "XXXXXXXXX@163.com"
    key dir：/home/hymnsun/.ssh/id_rsa
    ```
### [blog](https://blog.csdn.net/Arisstz/article/details/80708851)
- 安装nodejs和npm
    ```
    sudo apt-get install nodejs npm
    ```
- 配置环境变量
- 


### python_basic

-------
## BUG
- [x] 无法安装texstudio for linux 导致系统锁死
    >  sudo apt --fix-broken install

- 08/17 in MSI 卡死，键盘没反应，鼠标延迟高卡死，怀疑在后台更新系统

------
## what to do
- 梯子