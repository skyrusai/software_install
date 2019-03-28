http://dblab.xmu.edu.cn/blog/install-hbase/

sudo tar -zxf ~/Downloads/hbase-1.2.11-bin.tar.gz -C /usr/local
sudo mv /usr/local/hbase-1.2.11 /usr/local/hbase

gedit ~/.bashrc

export PATH=$PATH:/usr/local/hbase/bin

cd /usr/local
sudo chown -R hadoop ./hbase       #将hbase下的所有文件的所有者改为hadoop，hadoop是当前用户的用户名。

/usr/local/hbase/bin/hbase version



以下先决条件很重要，比如没有配置JAVA_HOME环境变量，就会报错。
– jdk
– Hadoop( 单机模式不需要，伪分布式模式和分布式模式需要)
– SSH

gedit /usr/local/hbase/conf/hbase-env.sh


gedit /usr/local/hbase/conf/hbase-site.xml

ssh localhost
cd /usr/local/hadoop
./sbin/start-dfs.sh

bin/hbase shell

增删改查

create 'student','Sname','Ssex','Sage','Sdept','course'
put 'teacher','91001','username','Mary'
put 'teacher','91001','username','Mary1'
put 'teacher','91001','username','Mary2'
put 'teacher','91001','username','Mary3'
put 'teacher','91001','username','Mary4'  
put 'teacher','91001','username','Mary5'

delete 'student','95001','Ssex'
deleteall 'student','95001'

get 'student','95001'
scan 'student'


disable 'student'  
drop 'student'

exit