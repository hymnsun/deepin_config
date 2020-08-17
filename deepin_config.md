# deepin v20体验 {ignore}
[TOC]

### 设置
- 终端ctrl+C不要修改
- 系统字体为Noto Serif CJK JP

--------------
## 软件
### 基础软件
- 讯飞输入法，英文键盘和讯飞 切换输入法ctrl+space
- 微信 TIM
- wps
- 迅雷
- 向日葵
- 网易云音乐
- aria2
    - install aria2:`sudo apt-get install aria2`
    - download aria2 file contain `.conf`,`.log`,`.session` file
    - modify `.conf` file which links to download dir & RPC secret token
    - run aria2 via `aria2c --conf-path='/home/hymnsun/aria2/aria2.conf'`
    - download [AriaNg(front-end)](https://github.com/mayswind/AriaNg/releases) from Github.
    - click `index.html` to fill in RPC secret token in AriaNg settings.
    - download BaidunYun 

`
### 工作软件
#### anaconda
- `conda info`
    安装路径： /home/hymnsun/anaconda3
- `conda env list`
    ```    
    conda create -n tf10 python=3.7 numpy pandas tensorflow=1.15
    conda remove -n <env_name> --all
    conda activate tf10
    conda deactivate
    ```
- conda 更换国内源

    - 修改 ~/.condarc文件，复制USTC源路径
        ```
        channels:
            - https://mirrors.ustc.edu.cn/anaconda/pkgs/main/
            - https://mirrors.ustc.edu.cn/anaconda/pkgs/free/
            - https://mirrors.ustc.edu.cn/anaconda/cloud/conda-forge/
            - defaults
        ssl_verify: true
        ```
    - terminel
        ```
        conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
        conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
        conda config --set show_channel_urls yes
        ```

    - 恢复默认源：
        `conda config --remove-key channels`

- 修改jupyter notebook工作路径：
    ```
    jupyter notebook --generate-config
    cd ~
    mkdir jupytercode
    vi /home/hymnsun/.jupyter/jupyter_notebook_config.py
    ```
    c.NotebookApp.notebook_dir =''

- [jupyter notebook 添加其它环境kernel](https://blog.csdn.net/wyz6666/article/details/83314761)
    ```
    conda activate tf10
    which python       // 当前环境python路径
    sudo <python dir> -m ipykernel install --name <kernel_name>
    ```

#### pycharm
- tips of the day
- 设置ctrl+鼠标放大
- Show line numbers          // right click 
- 设置python intepreter



#### texlive
- 中文环境设置
- texstudio安装报错

#### chrome
#### vscode
- ctrl+shift+K 删除当前行
- alt+鼠标左键 选中多行
- 插件：MPE
    


        
-------------
## LINUX 指令
    新建一个md文件
    pwd 显示当前路径
    ls -a 显示所有文件
    ls -la 且显示权限等详细信息
    mkdir <dir_name> 创建目录

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
### blog

### python_basic