## 3. shell
### 基础
- `shell` and `shell script`
- 文本首行增加`#!/bin/bash`,文本后缀名称无影响，主流便识性后缀`.sh`
- run 
    - `bash xxx.sh`
    - `chmod +x xxx.sh && ./xxx.sh`
- `source filename`,`. filename`,`bash filename`,`./filename`



### 需求
- 个人网站
    - 设计技术：网站、`子网穿透/反向代理`
        - 反向代理：保证内网的安全，通常将反向代理作为公网访问地址，Web 服务器是内网
    - 布局在内网个人pc上，用子网穿透通过公网ip访问
    - 直接布局在国外服务器上

- 个人文件服务器
    - 不清楚同一台电脑上的文件服务器和个人网站是如何独立访问的，是映射到计算机的不同端口上吗？
    - 是否涉及到`负载均衡`