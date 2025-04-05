# HW-8


https://get.jenkins.io/war-stable/latest/
sudo apt install openjdk-11-jdk
firewall-cmd --permanent --zone=public --add-port=8087/tcp
firewall-cmd --reload
java -jar jenkins.war --httpPort=8087


https://get.jenkins.io/war-stable/2.346.3/


✅ 删除 Jenkins 插件的方式
Jenkins 的插件都存放在主目录下的 plugins/ 文件夹中。删除这个文件夹中的内容即可移除所有插件。

🧹 步骤一：关闭 Jenkins
bash
复制
编辑
# 如果你是用命令行启动 Jenkins 的，可以直接 Ctrl+C 结束进程
# 或者用系统服务的方式关闭
sudo systemctl stop jenkins
🗑️ 步骤二：删除插件目录下的所有插件
bash
复制
编辑
cd ~/.jenkins/plugins
rm -rf *
也可以删除整个插件目录：

bash
复制
编辑
rm -rf ~/.jenkins/plugins


cd ~/.jenkins

