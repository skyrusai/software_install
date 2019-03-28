java

------------------

tar -zxvf jdk-8u201-linux-x64.tar.gz

sudo mv jdk1.8.0_201 /opt/

sudo gedit ~/.bashrc
在最末尾添加如下配置：
#set Java environment
export JAVA_HOME=/opt/jdk1.8.0_201
export JRE_HOME=${JAVA_HOME}/jre
export CLASSPATH=.:${JAVA_HOME}/lib:${JRE_HOME}/lib
export PATH=${JAVA_HOME}/bin:$PATH

source ~/.bashrc

java -version
