# Ubuntu 源设置


## 介绍

- 简单地讲：修改资源源地址主要是为了加快下载速度，默认的资源源地址在是境外，速度肯定没有境内速度快。
- 了解源这东西：<http://wiki.ubuntu.org.cn/%E6%BA%90%E5%88%97%E8%A1%A8>
- 文章的重点是页面最下面，每个版本的源地址都是不一样的，所以要懂得替换对应的版本英文名称，各个版本的英文名称大家自己找下，然后进行修改。


## 修改源

- 国内常用源配置方法：
    - 163 源：<http://mirrors.163.com/.help/ubuntu.html> 
    - 阿里源：<http://mirrors.aliyun.com/help/ubuntu>
    - sohu：<http://mirrors.sohu.com/help/ubuntu.html>
- 替换过程（更换之前最好备份一下 sources.list 配置文件）：
- 我以 Ubuntu 14.04 为例，使用网易源：
    - 备份下：`sudo cp /etc/apt/sources.list /etc/apt/sources_20151128_back.list`
    - 用 gedit 编辑器打开配置文件：`sudo gedit /etc/apt/sources.list`，替换里面所有内容为下面这些内容：
    ``` ini
    deb http://mirrors.163.com/ubuntu/ trusty main restricted universe multiverse
    deb http://mirrors.163.com/ubuntu/ trusty-security main restricted universe multiverse
    deb http://mirrors.163.com/ubuntu/ trusty-updates main restricted universe multiverse
    deb http://mirrors.163.com/ubuntu/ trusty-proposed main restricted universe multiverse
    deb http://mirrors.163.com/ubuntu/ trusty-backports main restricted universe multiverse
    deb-src http://mirrors.163.com/ubuntu/ trusty main restricted universe multiverse
    deb-src http://mirrors.163.com/ubuntu/ trusty-security main restricted universe multiverse
    deb-src http://mirrors.163.com/ubuntu/ trusty-updates main restricted universe multiverse
    deb-src http://mirrors.163.com/ubuntu/ trusty-proposed main restricted universe multiverse
    deb-src http://mirrors.163.com/ubuntu/ trusty-backports main restricted universe multiverse
    ```
    - 更换源之后，需要在终端中执行：`sudo apt-get update`，这是必须做的，不然你后面可能会遇到 apt-get 安装会提示：未发现软件包。
    
## 三：ubuntu各个版本的阿里云源内容
# 系统版本：ubuntu16.04

# 3.1.1：阿里源：

deb-src http://archive.ubuntu.com/ubuntu xenial main restricted #Added by software-properties
deb http://mirrors.aliyun.com/ubuntu/ xenial main restricted
deb-src http://mirrors.aliyun.com/ubuntu/ xenial main restricted multiverse universe #Added by software-properties
deb http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-updates main restricted multiverse universe #Added by software-properties
deb http://mirrors.aliyun.com/ubuntu/ xenial universe
deb http://mirrors.aliyun.com/ubuntu/ xenial-updates universe
deb http://mirrors.aliyun.com/ubuntu/ xenial multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-updates multiverse
deb http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-backports main restricted universe multiverse #Added by software-properties
deb http://archive.canonical.com/ubuntu xenial partner
deb-src http://archive.canonical.com/ubuntu xenial partner
deb http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted
deb-src http://mirrors.aliyun.com/ubuntu/ xenial-security main restricted multiverse universe #Added by software-properties
deb http://mirrors.aliyun.com/ubuntu/ xenial-security universe
deb http://mirrors.aliyun.com/ubuntu/ xenial-security multiverse

# 3.1.2：东北大学：

deb-src http://mirror.neu.edu.cn/ubuntu/ xenial main restricted #Added by software-properties
deb http://mirror.neu.edu.cn/ubuntu/ xenial main restricted
deb-src http://mirror.neu.edu.cn/ubuntu/ xenial restricted multiverse universe #Added by software-properties
deb http://mirror.neu.edu.cn/ubuntu/ xenial-updates main restricted
deb-src http://mirror.neu.edu.cn/ubuntu/ xenial-updates main restricted multiverse universe #Added by software-properties
deb http://mirror.neu.edu.cn/ubuntu/ xenial universe
deb http://mirror.neu.edu.cn/ubuntu/ xenial-updates universe
deb http://mirror.neu.edu.cn/ubuntu/ xenial multiverse
deb http://mirror.neu.edu.cn/ubuntu/ xenial-updates multiverse
deb http://mirror.neu.edu.cn/ubuntu/ xenial-backports main restricted universe multiverse
deb-src http://mirror.neu.edu.cn/ubuntu/ xenial-backports main restricted universe multiverse #Added by software-properties
deb http://archive.canonical.com/ubuntu xenial partner deb-src http://archive.canonical.com/ubuntu xenial partner
deb http://mirror.neu.edu.cn/ubuntu/ xenial-security main restricted
deb-src http://mirror.neu.edu.cn/ubuntu/ xenial-security main restricted multiverse universe #Added by software-properties
deb http://mirror.neu.edu.cn/ubuntu/ xenial-security universe
deb http://mirror.neu.edu.cn/ubuntu/ xenial-security multiverse

# 3.1.3：清华大学：

deb http://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial main restricted
deb http://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-updates main restricted
deb http://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial universe
deb http://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-updates universe
deb http://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial multiverse
deb http://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-updates multiverse
deb http://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-backports main restricted universe multiverse
deb http://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-security main restricted
deb http://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-security universe deb http://mirrors.tuna.tsinghua.edu.cn/ubuntu/ xenial-security multiverse

## 3.2：ubuntu 14.04 
# 3.2.1：Ubuntu 官方更新服务器（欧洲，此为官方源，国内较慢，但无同步延迟问题，电信、移动/铁通、联通等公网用户可以使用)：

deb http://archive.ubuntu.com/ubuntu/ trusty main restricted universe multiverse
deb http://archive.ubuntu.com/ubuntu/ trusty-security main restricted universe multiverse
deb http://archive.ubuntu.com/ubuntu/ trusty-updates main restricted universe multiverse
deb http://archive.ubuntu.com/ubuntu/ trusty-proposed main restricted universe multiverse
deb http://archive.ubuntu.com/ubuntu/ trusty-backports main restricted universe multiverse
deb-src http://archive.ubuntu.com/ubuntu/ trusty main restricted universe multiverse
deb-src http://archive.ubuntu.com/ubuntu/ trusty-security main restricted universe multiverse
deb-src http://archive.ubuntu.com/ubuntu/ trusty-updates main restricted universe multiverse
deb-src http://archive.ubuntu.com/ubuntu/ trusty-proposed main restricted universe multiverse
deb-src http://archive.ubuntu.com/ubuntu/ trusty-backports main restricted universe multiverse

Ubuntu官方提供的其他软件（第三方闭源软件等）：

deb http://archive.canonical.com/ubuntu/ trusty partner
deb http://extras.ubuntu.com/ubuntu/ trusty main
# 3.2.2：阿里云：

deb http://mirrors.aliyun.com/ubuntu/ trusty main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ trusty-security main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ trusty-updates main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ trusty-proposed main restricted universe multiverse
deb http://mirrors.aliyun.com/ubuntu/ trusty-backports main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ trusty main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-security main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-updates main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-proposed main restricted universe multiverse
deb-src http://mirrors.aliyun.com/ubuntu/ trusty-backports main restricted universe multiverse
