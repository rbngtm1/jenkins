#### Intallation command
#### Once you are in virtual machine, check in
  * ps -ef | grep java
  * df -k .
  * sudo yum install java-1.8.0-openjdk  --download all java related package.
  * wget https://archive.apache.org/dist/tomcat/tomcat-9/v9.0.0.M10/bin/apache-tomcat-9.0.0.M10.tar.gz
  * ls -lrt 
  * untar the gz file 
  * tar -xvf apache-tomcat-9.0.0.M10.tar.gz
  * ls -lrt
  * you can remove .gz file
  * rm apache-tomcat-9.0.0.M10.tar.gz -- as you already have a directory
  * mv apache-tomcat-9.0.0.M10 tomcat9 -- so that you can easily identify
  * cd tomcat9/
  * cd bin/
  * you will see startup.bat which is for windows and startup.sh for linux machine
  * ps -ef | grep tomcat
  * cd .. -- goto tomcat9
  * cd conf
  * less server.xml --see the connector port 
  
