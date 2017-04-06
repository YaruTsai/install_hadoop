#Docker executable
docker run -ti -d --name hadoop -p 9000:9000 -p 9001:9001 -p 50070:50070 ubuntu:16.04 /bin/bash

#Docker entry
docker exec -ti hadoop /bin/bash

#Goto Hadoop container
apt-get update
apt-get install openssh-server
cp /etc/ssh/sshd_config /etc/ssh/sshd_config.factory-defaults

apt-get install vim -y
ssh-keygen -t rsa -P ""
cat $HOME/.ssh/id_rsa.pub >> $HOME/.ssh/authorized_keys
ssh localhost

add-apt-repository ppa:webupd8team/java
apt-get install software-properties-common
apt-get install software-properties-common
add-apt-repository ppa:webupd8team/java
apt-get update
apt-get install oracle-java8-installer
java -version

apt-get install wget
cd ~
wget http://ftp.tc.edu.tw/pub/Apache/hadoop/common/hadoop-2.7.3/hadoop-2.7.3.tar.gz
tar xzvf hadoop-2.7.0.tar.gz
tar -xzvf hadoop-2.7.3.tar.gz
mkdir /usr/local/hadoop
mv hadoop-2.7.3 /usr/local/hadoop/
cd /usr/local/hadoop/
vim ~/.bashrc 
source ~/.bashrc

vim hadoop-env.sh
mkdir -p /app/hadoop/tmp


cd /usr/local/hadoop/hadoop-2.7.3/etc/hadoop
vim core-site.xml
cp mapred-site.xml.template mapred-site.xml
vim mapred-site.xml
vim yarn-site.xml
mkdir -p /usr/local/hadoop_store/hdfs/namenode
mkdir -p /usr/local/hadoop_store/hdfs/datanode
vim hdfs-site.xml
hdfs namenode -format
start-dfs.sh
start-yarn.sh
jps# install_hadoop
