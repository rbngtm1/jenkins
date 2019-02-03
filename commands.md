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
  * cd conf -- here there is file called server.xml where there is section called connector port 
  * less server.xml --see the connector port or vi server.xml and you can change the port number too
  * if you made changes to port, restart the tomcat -- cd ..     cd bin/     ./startup.sh  ./shutdown.sh   ./startup.sh
  * go outside the tomcat9 and install jenkins
  * wget http://updates.jenkins-ci.org/download/war/2.100/jenkins.war
  * cp jenkins.war /home/ec2-user/tomcat9/webapps/
  * sudo cat /home/ec2-user/.jenkins/secrets/initialAdmin  and get the password and paste
