# OOS
运维部署

+ [单机]
+ [分布式]

## 基础系统配置

+ 推荐内存4G/硬盘50G以上
+ 最小化安装`CentOS 7 Minimal`
+ 配置基础网络、更新源、SSH登陆等

## 安装依赖工具

CentOS 7 请执行以下脚本：

``` bash
# 文档中脚本默认均以root用户执行
# 安装 epel 源
yum install epel-release -y
# 安装依赖工具
yum install git python python-pip -y
```

``` bash
# 安装ansible (国内如果安装太慢可以直接用pip阿里云加速)
pip install pip --upgrade -i http://mirrors.aliyun.com/pypi/simple/ --trusted-host mirrors.aliyun.com
pip install --no-cache-dir ansible -i http://mirrors.aliyun.com/pypi/simple/ --trusted-host mirrors.aliyun.com
pip install pip --upgrade
pip install ansible
# 配置ansible ssh密钥登陆
ssh-keygen -t rsa -b 2048 回车 回车 回车
ssh-copy-id $IP #$IP为本机地址，按照提示输入yes 和root密码
```

