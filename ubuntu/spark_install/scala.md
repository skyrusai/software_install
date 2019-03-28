http://dblab.xmu.edu.cn/blog/929-2/

sudo tar -zxf ~/Downloads/scala-2.11.12.tgz -C /usr/local   # 解压到/usr/local中
cd /usr/local/
sudo mv ./scala-2.11.12/ ./scala         # 将文件夹名改为scala
sudo chown -R hadoop ./scala        # 修改文件权限，用hadoop用户拥有对scala目录的权限

gedit ~/.bashrc