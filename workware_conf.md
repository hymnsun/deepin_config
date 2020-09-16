[TOC]

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
- 修改jupyter notebook工作路径：
    `cd ~`
    `mkdir jupytercode`
    `vi /home/hymnsun/.jupyter/jupyter_notebook_config.py`
        c.NotebookApp.notebook_dir =''

#### pycharm
- python脚本设置
    ```
    #!/usr/bin/python
    # -*- coding: utf-8 -*-
    ```

- [jupyter notebook 添加其它环境kernel](https://blog.csdn.net/wyz6666/article/details/83314761)
    ```
    conda activate tf10
    which python       // 当前环境python路径
    sudo <python dir> -m ipykernel install --name <kernel_name>
    ```

- 基础设置
    - tips of the day
    - 设置ctrl+鼠标放大
    - Show line numbers          // right click 
    - 设置python intepreter

#### v2Ray
- ~~download `v2ray-linux-64.zip` in [Github](https://github.com/v2ray/v2ray-core/releases/)~~
- ~~download `go.sh` via `wget https://install.direct/go.sh`~~
- ~~在上述两个文件同一目录下，run `sudo bash go.sh --local ./v2ray-linux-64.zip`~~
- 根据提示https://install.direct/go.sh已弃用
![https://github.com/v2fly/fhs-install-v2ray](./v2ray/v2ray_conf.png)

    这种方法配置文件分成了多个`/usr/local/etc/v2ray` 不会处理
    
- [**使用原来的go.sh文件**](https://www.280i.com/case/7935.html)
    下载失败注意修改*DOWNLOAD_LINK=*
    - run `sudo bash go.sh` in dir contains go.sh
    - edit `config.json` in `/etc/v2ray/config.json` file which can copy from windows
    ![v2ray](./v2ray/v2ray_file.png)
    - 设置自启动，查看状态
        ```
        启动 `systemctl start v2ray`
        停止 `systemctl stop v2ray`
        重启 `systemctl restart v2ray`
        开机自启 `systemctl enable v2ray`
        查看状态 `service v2ray status`
        ```
    - 配置代理时报错？？？？

#### texlive2020
- [error log](./config_log.md)
- [linux完全卸载texlive](https://blog.csdn.net/qq_40199232/article/details/106505730)
    ```
    sudo apt-get purge texlive*
    rm -rf /usr/local/texlive/2020
    rm -rf ~/.texlive2020
    rm -rf /usr/local/share/texmf
    rm -rf /var/lib/texmf
    rm -rf /etc/texmf
    sudo apt-get remove tex-common --purge
    rm -rf ~/.texlive
    ```
- [下载texlive2020镜像](http://iso.mirrors.ustc.edu.cn/CTAN/systems/texlive/Images/texlive2020-20200406.iso)

- [install]((https://www.cnblogs.com/lzhu/p/10457162.html))
    ```
    sudo mount -o loop [texlive2020.iso] /mnt/
    cd /mnt/
    sudo ./install-tl --gui
    ```
    ![install](./tex/texlive_install.png)

- 卸载镜像`sudo umount /mnt`
- 添加环境变量
    - run `dedit ./bashrc`
    - copy the cotent bellow,save and exit
        ```
        # TeX Live 2020
        PATH=/usr/local/texlive/2020/bin/x86_64-linux:$PATH; export PATH
        MANPATH=/usr/local/texlive/2020/texmf-dist/doc/man:$MANPATH; export MANPATH
        INFOPATH=/usr/local/texlive/2020/texmf-dist/doc/info:$INFOPATH; export INFOPATH
        ```
    - run `source ~/.bashrc` to make it work
    - test in terminal via `tex -v`
- 测试{xeCJK}和包更新
    - `sudo apt-get install texlive-xetex`      # 测试是否需要
    - `sudo apt-get install texlive-lang-chinese`        #{xeCJK}
    ![缺少CJK默认中文字体](./tex/cjk.png)
    - 修改xelatex路径解决包识别
    ![xelatex配置](./tex/texstudio_config.png)

#### chrome
#### vscode
- ctrl+shift+K 删除当前行
- alt+鼠标左键 选中多行
- 插件：MPE