# 常⽤linux命令⼿册
```shell
# 即刻关机
shutdown -h now 
```

```shell
# 10分钟后关机 
shutdown -h 10 
```

```shell
# 11：00关机 
shutdown -h 11:00 
```

```shell
# 预定时间关机（10分钟后）
shutdown -h +10  
```

```shell
# 取消指定时间关机 
shutdown -c 
```

```shell
# 重启 
shutdown -r now 
```

```shell
# 10分钟之后重启 
shutdown -r 10 
```

```shell
# 定时重启 
shutdown -r 11:00 
```

```shell
# 重启 
reboot 
```

```shell
# 重启 
init 6 
```

```shell
# ⽴刻关机
init 0  
```

```shell
# 关机 
telinit 0 
```

```shell
# ⽴刻关机 
poweroff 
```

```shell
# 关机 
halt 
```

```shell
# buff数据同步到磁盘
sync 
```

```shell
# 退出登录Shell 
logout 
```

```shell
# 查看内核/OS/CPU信息
uname -a 
```

```shell
# 查看内核版本 
uname -r 
```

```shell
# 查看处理器架构 
uname -m 
```

```shell
# 查看处理器架构 
arch 
```

```shell
# 查看计算机名
hostname 
```

```shell
# 显示当前登录系统的⽤户 
who 
```

```shell
# 显示登录时的⽤户名
who am i  
```

```shell
# 显示当前⽤户名
whoami  
```

```shell
# 查看linux版本信息 
cat /proc/version 
```

```shell
# 查看CPU信息 
cat /proc/cpuinfo 
```

```shell
# 查看中断 
cat /proc/interrupts 
```

```shell
# 查看系统负载 
cat /proc/loadavg 
```

```shell
# 查看系统运⾏时间、⽤户数、负载 
uptime 
```

```shell
# 查看系统的环境变量
env  
```

```shell
# 查看系统USB设备信息
lsusb -tv  
```

```shell
# 查看系统PCI设备信息 
lspci -tv 
```

```shell
# 查看已加载的系统模块
lsmod 
```

```shell
# 系统信息和性能查看
grep MemTotal /proc/meminfo 
```

```shell
# 查看空闲内存量 
grep MemFree /proc/meminfo 
```

```shell
# 查看内存⽤量和交换区⽤量 
free -m 
```

```shell
# 显示系统⽇期时间 
date 
```

```shell
# 显示2021⽇历表 
cal 2021 
```

```shell
# 动态显示cpu/内存/进程等情况 
top 
```

```shell
# 每1秒采⼀次系统状态，采20次
vmstat 1 20 
```

```shell
# 查看io读写/cpu使⽤情况 
iostat 
```

```shell
# 查询cpu使⽤情况（1秒⼀次，共10次）
sar -u 1 10 
```

```shell
# 查询磁盘性能常⽤命令 
sar -d 1 10 
```

```shell
# 查看所有磁盘分区
fdisk -l 
```

```shell
# 查看所有交换分区 
swapon -s 
```

```shell
# 查看磁盘使⽤情况及挂载点
df -h 

# 同上 
df -hl 
```

```shell
# 查看指定某个⽬录的⼤⼩ 
du -shell /dir 
```

```shell
# 从⾼到低依次显示⽂件和⽬录⼤⼩
du -sk * | sort -rn  
```

```shell
# 挂载hda2盘 
mount /dev/hda2 /mnt/hda2 
```

```shell
# 指定⽂件系统类型挂载（如ntfs） 
mount -t ntfs /dev/sdc1 /mnt/usbhd1 
```

```shell
# 挂载iso⽂件 
mount -o loop xxx.iso /mnt/cdrom 
```

```shell
# 挂载usb盘/闪存设备 
mount /dev/sda1 /mnt/usbdisk 
```

```shell
# 通过设备名卸载 
umount -v /dev/sda1 
```

```shell
# 通过挂载点卸载 
umount -v /mnt/mymnt 
```

```shell
# 强制卸载(慎⽤) 
fuser -km /mnt/hda1 
```

```shell
# 创建⽤户 
useradd dsjprs
```

```shell
# 删除⽤户
userdel -r dsjprs
```

```shell
# 修改⽤户的组 
usermod -g group_name user_name 
```

```shell
# 将⽤户添加到组 
usermod -aG group_name user_name 
```

```shell
# 修改⽤户codesheep的登录Shell、
usermod -s /bin/ksh -d /home/dsjprs
 
# 主⽬录以及⽤户组 
–g devdsjprs
```

```shell
# 查看test⽤户所在的组
groups test 
```

```shell
# 创建⽤户组 
groupadd group_name 
```

```shell
# 删除⽤户组 
groupdel group_name 
```

```shell
# 重命名⽤户组 
groupmod -n new_name old_name 
```

```shell
# 完整切换到⼀个⽤户环境
su - user_name 
```

```shell
# 修改某⽤户的⼝令 
passwd dsjprs
```

```shell
# 查看活动⽤户 
w 
```

```shell
# 查看指定⽤户codesheep信息 
id codesheep 
```

```shell
# 查看⽤户登录⽇志 
last 
```

```shell
# 查看当前⽤户的计划任务
crontab -l 
```

```shell
# 查看系统所有⽤户 
cut -d: -f1 /etc/passwd 
```

```shell
# 查看系统所有组 
cut -d: -f1 /etc/group 
```

```shell
# 查看⽹络接⼝属性
ifconfig 
```

```shell
# 查看某⽹卡的配置
ifconfig eth0 
```

```shell
# 查看路由表
route -n 
```

```shell
# 查看所有监听端⼝
netstat -lntp  
```

```shell
# 查看已经建⽴的TCP连接 
netstat -antp 
```

```shell
# 查看TCP/UDP的状态信息 
netstat -lutp 
```

```shell
# 启⽤eth0⽹络设备 
ifup eth0 
```

```shell
# 禁⽤eth0⽹络设备 
ifdown eth0 
```

```shell
# 查看iptables规则 
iptables -L 
```

```shell
# 配置ip地址 
dhclient eth0 
```

```shell 
# 以dhcp模式启⽤eth0 
route add -net 0/0 gw Gateway_IP 
```

```shell
# 删除静态路由 
route del 0/0 gw Gateway_IP 
```

```shell
# 查看主机名 
hostname 
```

```shell
# 解析主机名 
host www....
```

```shell
# 查询DNS记录，查看域名解析是否正常 
nslookup com......
```

```shell
# 查看所有进程 
ps -ef 
```

```shell
# 过滤出你需要的进程 
ps -ef | grep codesheep 
```

```shell
# kill指定名称的进程 
kill -s name 
```

```shell
# kill指定pid的进程 
kill -s pid 
```

```shell
# 实时显示进程状态 
top 
```

```shell
# 每1秒采⼀次系统状态，采20次 
vmstat 1 20 
```

```shell
# 查看io读写/cpu使⽤情况 
iostat 
```

```shell
# 查询cpu使⽤情况（1秒⼀次，共10次）
sar -u 1 10 
```

```shell
# 查询磁盘性能常⽤命令 
sar -d 1 10 
```

```shell
# 列出系统服务
chkconfig --list  
```

```shell
# 查看某个服务
service <服务名> status 
```

```shell
# 启动某个服务 
service <服务名> start 
```

```shell
# 终⽌某个服务
service <服务名> stop 
```

```shell
# 重启某个服务 
service <服务名> restart 
```

```shell
# 查看某个服务 
systemctl status <服务名> 
```

```shell
# 启动某个服务 
systemctl start <服务名> 
```

```shell
# 终⽌某个服务 
systemctl stop <服务名> 
```

```shell
# 重启某个服务
systemctl restart <服务名> 
```

```shell
# 开启⾃启动 
systemctl enable <服务名> 
```

```shell
# 关闭⾃启动 
systemctl disable <服务名> 
```

```shell
# 进⼊某个⽬录 
cd <⽬录名> 
```

```shell
# 回上级⽬录 
cd .. 
```

```shell
# 回上两级⽬录
cd ../..  
```

```shell
# 进个⼈主⽬录 
cd 
```

```shell
# 回上⼀步所在⽬录
cd - 
```

```shell
# 显示当前路径
pwd 
```

```shell
# 查看⽂件⽬录列表 
ls 
```

```shell
# 查看⽬录中内容（显示是⽂件还是⽬录）
ls -F 
```

```shell
# 查看⽂件和⽬录的详情列表 
ls -l 
```

```shell
# 查看隐藏⽂件 
ls -a 
```

```shell
# 查看⽂件和⽬录的详情列表（增强⽂件⼤⼩易读性）
ls -lh 
```

```shell
# 查看⽂件和⽬录列表（以⽂件⼤⼩升序查看）
ls -lSr 
```

```shell
# 查看⽂件和⽬录的树形结构 
tree 
```

```shell
# 创建⽬录 
mkdir <⽬录名> 
```

```shell
# 同时创建两个⽬录 
mkdir dir1 dir2 
```

```shell
# 创建⽬录树 
mkdir -p /tmp/dir1/dir2 
```

```shell
# 删除'file1'⽂件 
rm -f file1 
```

```shell
# 删除'dir1'⽬录 
rmdir dir1 
```

```shell
# 删除'dir1'⽬录和其内容 
rm -rf dir1 
```

```shell
# 同时删除两个⽬录及其内容 
rm -rf dir1 dir2 
```

```shell
# 重命名/移动⽬录 
mv old_dir new_dir 
```

```shell
# 复制⽂件 
cp file1 file2 
```

```shell
#复制某⽬录下的所有⽂件⾄当前⽬录
cp dir/* . 
```

```shell
# 复制⽬录 
cp -a dir1 dir2 
```

```shell
# 复制⼀个⽬录⾄当前⽬录 
cp -a /tmp/dir1 . 
```

```shell
# 创建指向⽂件/⽬录的软链接 
ln -s file1 link1 
```

```shell
# 创建指向⽂件/⽬录的物理链接
ln file1 lnk1 
```

```shell
# 从根⽬录开始搜索⽂件/⽬录 
find / -name file1 
```

```shell
# 搜索⽤户user1的⽂件/⽬录 
find / -user user1 
```

```shell
# 在⽬录/dir中搜带有.bin后缀的⽂件 
find /dir -name *.bin 
```

```shell
# 寻找.mp4结尾的⽂件 
locate *.mp4 
```

```shell
# 显示某⼆进制⽂件/可执⾏⽂件的路径
whereis <关键词> 
```

```shell
# 查找系统⽬录下某的⼆进制⽂件 
which <关键词> 
```

```shell
# 设置⽬录所有者(u)、群组(g)及其他⼈(o)的读(r)写(w) 执⾏(x) 权限 
chmod ugo+rwx dir1 
```

```shell
# 移除群组(g)与其他⼈(o)对⽬录的读写执⾏权限 
chmod go-rwx dir1 
```

```shell
# 改变⽂件的所有者属性
chown user1 file1 
```

```shell
# 改变⽬录的所有者属性 
chown -R user1 dir1
```

```shell
# 改变⽂件群组chown 
chgrp group1 file1 
```

```shell
# 改变⽂件的所有⼈和群组
user1:group1 file1
```

```shell
# 查看⽂件内容 
cat file1 
```

```shell
# 查看内容并标示⾏数 
cat -n file1 
```

```shell
# 从最后⼀⾏开始反看⽂件内容 
cat xxx.txt 
awk 'NR%2==1' tac file1 
```

```shell
# 查看⼀个⻓⽂件的内容 
more file1 
```

```shell
# 类似more命令，但允许反向操作 
less file1 
```

```shell
# 查看⽂件前两⾏ 
head -2 file1 
```

```shell
# 查看⽂件后两⾏ 
tail -2 file1 
```

```shell
# 实时查看添加到⽂件中的内容 
tail -f /log/msg 
```

```shell
# 在⽂件hello.txt中查找关键词dsjprs
grep dsjprs hello.txt 
```

```shell
# 在⽂件hello.txt中查找以prs开头的内容 
grep ^prs hello.txt 
```

```shell
# 选择hello.txt⽂件中所有包含数字的⾏
grep [0-9] hello.txt
```

```shell
# 将hello.txt⽂件中的s1替换成s2 
sed 's/s1/s2/g' hello.txt 
```

```shell
# 从hello.txt⽂件中删除所有空⽩⾏ 
sed '/^$/d' hello.txt 
```

```shell
# 从hello.txt⽂件中删除所有注释和空⽩⾏ 
sed '/ *#/d; /^$/d' hello.txt 
```

```shell
# 从⽂件hello.txt 中排除第⼀⾏ 
sed -e '1d' hello.txt 
```

```shell
# 查看只包含关键词"s1"的⾏ 
sed -n '/s1/p' hello.txt
```

```shell
# 删除每⼀⾏最后的空⽩字符 
sed -e 's/ *$//' hello.txt 
```

```shell
# 从⽂档中只删除词汇s1并保留剩余全部 
sed -e 's/s1//g' hello.txt 
```

```shell
# 查看从第⼀⾏到第5⾏内容 
sed -n '1,5p;5q' hello.txt 
```

```shell
# 查看第5⾏ 
sed -n '5p;5q' hello.txt 
```

```shell
# 合并两个⽂件或两栏的内容 
paste file1 file2 
```

```shell
 # 合并两个⽂件或两栏的内容，中间⽤"+"区分 
paste -d '+' file1 file2 
```

```shell
# 排序两个⽂件的内容 
sort file1 file2 
```

```shell
# ⽐较两个⽂件的内容(去除'file1'所含内容) 
comm -1 file1 file2 
```

```shell
# ⽐较两个⽂件的内容(去除'file2'所含内容)
comm -2 file1 file2 
```

```shell
# ⽐较两个⽂件的内容(去除两⽂件共有部分)常⽤命令 
comm -3 file1 file2 
```

```shell
# 压缩⾄zip包 
zip xxx.zip file 
```

```shell
# 将多个⽂件+⽬录压成zip包 
zip -r xxx.zip file1 file2 dir1 
```

```shell
# 解压zip包 
unzip xxx.zip
```

```shell
# 创建⾮压缩tar包 
tar -cvf xxx.tar file 
```

```shell
# 将多个⽂件+⽬录打tar包 
tar -cvf xxx.tar file1 file2 dir1 
```

```shell
# 查看tar包的内容 
tar -tf xxx.tar 
```

```shell
# 解压tar包 
tar -xvf xxx.tar
```

```shell
# 将tar包解压⾄指定⽬录 
tar -xvf xxx.tar -C /dir
```

```shell
# 创建bz2压缩包 
tar -cvfj xxx.tar.bz2 dir 
```

```shell
# 解压bz2压缩包 
tar -jxvf xxx.tar.bz2
```

```shell
# 创建gzip压缩包 
tar -cvfz xxx.tar.gz dir 
```

```shell
# 解压gzip压缩包 
tar -zxvf xxx.tar.gz 
```

```shell
# 解压bz2压缩包 
bunzip2 xxx.bz2 
```

```shell
# 压缩⽂件 
bzip2 filename 
```

```shell
# 解压gzip压缩包 
gunzip xxx.gz
```

```shell
# 压缩⽂件 
gzip filename 
```

```shell
# 最⼤程度压缩 打包和解压常⽤命令
gzip -9 filename 
```

```shell
# 查看已安装的rpm包 
rpm -qa 
```

```shell
# 查询某个rpm包 
rpm -q pkg_name
```

```shell
# 显示xxx功能是由哪个包提供的
rpm -q --whatprovides xxx 
```

```shell
# 显示xxx功能被哪个程序包依赖的 
rpm -q --whatrequires xxx 
```

```shell
# 显示xxx包的更改记录 
rpm -q --changelog xxx 
```

```shell
# 查看⼀个包的详细信息
rpm -qi pkg_name 
```

```shell
# 查询⼀个包所提供的⽂档
rpm -qd pkg_name 
```

```shell
 # 查看已安装rpm包提供的配置⽂件 
rpm -qc pkg_name 
```

```shell
# 查看⼀个包安装了哪些⽂件 
rpm -ql pkg_name 
```

```shell
# 查看某个⽂件属于哪个包
rpm -qf filename 
```

```shell
# 查询包的依赖关系 
rpm -qR pkg_name
```

```shell
# 安装rpm包 
rpm -ivh xxx.rpm 
```

```shell
# 测试安装rpm包 
rpm -ivh --test xxx.rpm
```

```shell
# 安装rpm包时忽略依赖关系 
rpm -ivh --nodeps xxx.rpm
```

```shell
# 卸载程序包 
rpm -e xxx 
```

```shell
# 升级确定已安装的rpm包 
rpm -Fvh pkg_name 
```

```shell
# 升级rpm包(若未安装则会安装) 
rpm -Uvh pkg_name 
```

```shell
# RPM包详细信息校验
rpm -V pkg_name 
```

```shell
# 显示可⽤的源仓库 
yum repolist enabled 
```

```shell
# 搜索软件包
yum search pkg_name 
```

```shell
# 下载并安装软件包 
yum install pkg_name
```

```shell
# 只下载不安装 
yum install --downloadonly pkg_name 
```

```shell
# 显示所有程序包 
yum list 
```

```shell
# 查看当前系统已安装包
yum list installed 
```

```shell
# 查看可以更新的包列表 
yum list updates 
```

```shell
# 查看可升级的软件包 
yum check-update 
```

```shell
# 更新所有软件包
yum update 
```

```shell
# 升级指定软件包 
yum update pkg_name 
```

```shell
# 列出软件包依赖关系 
yum deplist pkg_name 
```

```shell
# 删除软件包 
yum remove pkg_name 
```

```shell
# 清除缓存 
yum clean all 
```

```shell
# 清除缓存的软件包 
yum clean packages 
```

```shell
# 清除缓存的header 
yum clean headers
```

```shell
# 列出deb包的内容
dpkg -c xxx.deb 
```

```shell
# 安装/更新deb包 
dpkg -i xxx.deb 
```

```shell
# 移除deb包
dpkg -r pkg_name
```

```shell
# 移除deb包(不保留配置)
dpkg -P pkg_name 
```

```shell
# 查看系统中已安装deb包 
dpkg -l 
```

```shell
# 显示包的⼤致信息 
dpkg -l pkg_name 
```

```shell
# 查看deb包安装的⽂件 
dpkg -L pkg_name
```

```shell
# 查看包的详细信息 
dpkg -s pkg_name 
```

```shell
# 解开deb包的内容
dpkg –unpack xxx.deb 
```

```shell
# 搜索程序包 
apt-cache search pkg_name 
```

```shell
# 获取包的概览信息 
apt-cache show pkg_name 
```

```shell
# 安装/升级软件包
apt-get install pkg_name
```

```shell
# 卸载软件（包括配置）
apt-get purge pkg_name
```

```shell
# 卸载软件（不包括配置）
apt-get remove pkg_name 
```

```shell
# 更新包索引信息 
apt-get update 
```

```shell
# 更新已安装软件包
apt-get upgrade 
```

```shell
# 清理缓存 
apt-get clean
```

