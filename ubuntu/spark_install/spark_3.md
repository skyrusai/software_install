http://dblab.xmu.edu.cn/blog/1307-2/


sudo tar -zxf ~/Downloads/spark-2.4.0-bin-without-hadoop.tgz -C /usr/local/
cd /usr/local
sudo mv ./spark-2.4.0-bin-without-hadoop/ ./spark
sudo chown -R hadoop:hadoop ./spark          # 此处的 hadoop 为你的用户名

cd /usr/local/spark
cp ./conf/spark-env.sh.template ./conf/spark-env.sh

gedit ./conf/spark-env.sh

cd /usr/local/spark
bin/run-example SparkPi 2>&1 | grep "Pi is"

bin/spark-shell