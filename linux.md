# 总核数 = 物理CPU个数 X 每颗物理CPU的核数 
# 总逻辑CPU数 = 物理CPU个数 X 每颗物理CPU的核数 X 超线程数

# 查看物理CPU个数
cat /proc/cpuinfo| grep "physical id"| sort| uniq| wc -l

# 查看每个物理CPU中core的个数(即核数)
cat /proc/cpuinfo| grep "cpu cores"| uniq

# 查看逻辑CPU的个数
cat /proc/cpuinfo| grep "processor"| wc -l

# 查看CPU信息（型号）
cat /proc/cpuinfo | grep name | cut -f2 -d: | uniq -c

# 查看显卡的硬件信息 
lspci | grep -i vga

# 查看Linux内核版本命令(两种方法)
1. cat /proc/version
2. uname -a

# 查看Linux系统版本的命令(3种方法)
1. lsb_release -a, 即可列出所有版本信息.
2. cat /etc/redhat-release, 这种方法只适合Redhat系的Linux.
3. cat /etc/issue, 此命令也适用于所有的Linux发行版.

# 搜索用户目录下，超过800M大小的文件并删除
find ~ -type f -size +800M | xargs -n 1 -P 128 rm -f

# apt-get安装目录和安装路径
apt-get 下载后，软件所在路径是：/var/cache/apt/archives

ubuntu 默认的PATH为

PATH=/home/brightman/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games

apt-get install安装目录是包的维护者确定的，不是用户


#   dpkg -L +软件包的名字，可以知道这个软件包包含了哪些文件 
dpkg -L  libxml2

系统安装软件一般在/usr/share，可执行的文件在/usr/bin，配置文件可能安装到了/etc下等。

文档一般在 /usr/share

可执行文件 /usr/bin

配置文件 /etc

lib文件 /usr/lib
