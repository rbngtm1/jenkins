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
#### Integrating Jenkins with github
  * Create a newjob. You may name it samplejob, freestyle project
  * Go to Build and execute shell
  * type something like and save and build
    df -k .
    touch newfile
    ps -a
    echo "hello"
    
  * To configure github, to to manage Jenkins
  * Check in the global tool configuration
  * add maven and you may keep 3.5.3 as version as well as name, save and apply
  * Let's intall mannually but we may also Go to manage plugins ,On available, you can see all the plugins that are available; select       github and you can click install without restart, but another way is to install mannually 
  * sudo yum groupinstall "Development tools" on terminal 
  * wget https://github.com/git/git/archive/v2.7.2.tar.gz -O git.tar.gz
  * Extract by tar -xvf git.tar.gz
  * Go inside git directory 
  * make configure
  * pwd -- my home path is /home/ec2-user/git-2.7.2
  * ./configure -prefix=/home/ec2-user/git-2.7.2
  * sudo make install
  * git config --global user.name "Robin Gautam"
  * git config --global user.email "robin.awscloud.com"
  * to install the latest version of jenkins to integrate with github
  * try wget http://updates.jenkins-ci.org/download/war/2.109/jenkins.war
  * cd tomcat9/bin
  *  ./shutdown.sh
  *  mv /home/ec2-user/jenkins.war /home/ec2-user/tomcat9/webapps/.
  * cd ../bin
  * ./startup.sh
  * You can make changes in the back end and see those changes in front end
  * go inside .jenkins and jobs and (projectname) and config.xml ( vi config.xml) make changes in the build and restart using frontend by going to manage jenkins

