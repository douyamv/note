#linux基础知识

1. du -sh +文件目录     可以统计文件夹的大小
2. grep localhost /etc/hosts 可以在文本文件里搜索指定字符串
3. find  / -iname +文件名或者正则  可以在/目录循环查找不分大小写的文件
4. 

#apt-get安装时出现太多错误解决办法
    1.$ sudo mv /var/lib/dpkg/info /var/lib/dpkg/info_old //现将info文件夹更名
    2.$ sudo mkdir /var/lib/dpkg/info //再新建一个新的info文件夹
    3.$ sudo apt-get update, apt-get -f install //不用解释了吧
    4.$ sudo mv /var/lib/dpkg/info/* /var/lib/dpkg/info_old //执行完上一步操作后会在新的info文件夹下生成一些文件，现将这些文件全部移到info_old文件夹下
    5.$ sudo rm -rf /var/lib/dpkg/info //把自己新建的info文件夹删掉
    6.$ sudo mv /var/lib/dpkg/info_old /var/lib/dpkg/info //把以前的info文件夹重新改回名字
