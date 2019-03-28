
================
ssh

------------

sudo apt-get install openssh-server

ssh localhost

exit                           # 退出刚才的 ssh localhost
cd ~/.ssh/                     # 若没有该目录，请先执行一次ssh localhost
ssh-keygen -t rsa              # 会有提示，都按回车就可以
cat ./id_rsa.pub >> ./authorized_keys  # 加入授权


==================

sudo tar -zxf ~/Downloads/hadoop-2.7.7.tar.gz -C /usr/local    # 解压到/usr/local中
cd /usr/local/
sudo mv ./hadoop-2.7.7/ ./hadoop            # 将文件夹名改为hadoop
sudo chown -R hadoop ./hadoop       # 修改文件权限

cd /usr/local/hadoop
./bin/hadoop version

gedit ./etc/hadoop/core-site.xml

gedit ./etc/hadoop/hdfs-site.xml

./bin/hdfs namenode -format

./sbin/start-dfs.sh  #start-dfs.sh是个完整的可执行文件，中间没有空格


http://dblab.xmu.edu.cn/blog/install-hadoop/
