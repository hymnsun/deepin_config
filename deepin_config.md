[TOC]

# deepin v20体验
## 软件
    讯飞输入法，英文键盘和讯飞 切换输入法ctrl+space
    微信 TIM
    wps
    迅雷
    向日葵
    pycharm
        设置ctrl+鼠标放大
        设置python intepreter
    网易云音乐
    anaconda
        conda info
            安装路径： /home/hymnsun/anaconda3
        conda env list
            conda create -n tf10 python=3.7 numpy pandas tensorflow=1.15
            conda remove -n <env_name> --all
            conda activate tf10
            conda deactivate
        conda 更换国内源
        修改 ～/.condarc文件，复制USTC源路径
            channels:
                - https://mirrors.ustc.edu.cn/anaconda/pkgs/main/
                - https://mirrors.ustc.edu.cn/anaconda/pkgs/free/
                - https://mirrors.ustc.edu.cn/anaconda/cloud/conda-forge/
            ssl_verify: true
        修改jupyter notebook工作路径：
            vi /home/hymnsun/.jupyter/jupyter_notebook_config.py



    texlive

    chrome
    vscode
        ctrl+shift+K 删除当前行
        插件：MPE


## 设置
    系统字体为Noto Serif CJK JP
        

## LINUX 指令
    pwd 显示当前路径
    ls -a 显示所有文件
    ls -la 且显示权限等详细信息
    mkdir <dir_name> 创建目录

    VIM基本指令
        三种模式：
        查找：
        

    docker的配置

## Git管理
    git 连接github：
        ssh-keygen -t rsa -C "XXXXXXXXX@163.com"
        key dir：/home/hymnsun/.ssh/id_rsa


## BUG
    无法安装texstudio for LINUX
