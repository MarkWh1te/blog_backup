## 建立Jenkins 持续集成环境

* 下载安装Jenkins(on Ubuntu)

>wget -q -O - https://jenkins-ci.org/debian/jenkins-ci.org.key 

>sudo apt-key add -

>sudo sh -c 'echo deb http://pkg.jenkins-ci.org/debian-stable 

>binary/ > /etc/apt/sources.list.d/jenkins.list'

>sudo apt-get update

>sudo apt-get install jenkins

* 配置jenkins (配合django-jenkins)

jenkins安装后,会自动启动,默认是在8080
