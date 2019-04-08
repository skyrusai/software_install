https://docs.anaconda.com/anaconda/install/linux/

md5sum ~/Downloads/Anaconda3-5.2.0-Linux-x86_64.sh


sudo bash ~/Downloads/Anaconda3-5.2.0-Linux-x86_64.sh

python 3.6

sudo bash ~/Downloads/Anaconda3-5.3.1-Linux-x86_64.sh

python 3.7

source ~/.bashrc

conda create -n py35 python=3.5

source activate py35
conda activate py35

source deactivate

anaconda-navigator


https://mirrors.tuna.tsinghua.edu.cn/help/anaconda/

换源

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --set show_channel_urls yes

conda install cython