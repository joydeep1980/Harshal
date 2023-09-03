# Harshal
Created this as a task to create respository in github

How to install Jenkins in ubantu

Approach 4 :- Install Jenkins On Ubuntu

This installation is specific to systems operating on Ubuntu.   Follow the below steps:  https://www.jenkins.io/doc/book/installing/linux/ 
Step 1: Install Java                           
$ sudo apt update && sudo apt-get install openjdk-11-jdk-headless -y
Step 2: Add Jenkins Repository i.e key
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
Step 3: Add Jenkins repo to the system i.e source list
$  echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
Step 4: Install Jenkins
$ sudo apt update && sudo apt install jenkins -y
Step 5: Verify installation
$ systemctl status jenkins
Step 6: Once Jenkins is up and running, access it from the
link: http://localhost:8080    or the IP of virtual machine like xx.xx.xx.xx:8080

Get the initial admin pwd from command  cat /var/lib/jenkins/secrets/initialAdminPassword  (PWD-5986566625f04c89b2382094663f50dc) 
Start, Stop & Restart Jenkins
$ sudo service jenkins restart
$ sudo service jenkins stop
$ sudo service jenkins start

Step 7 :  apt install maven
