## Jenkins Installation on AWS EC2 Instance
 Before installing jenkins, launch EC2 instance
 
 Now Let see installtion part step by step.
 
 1. Update the packages
 
 ```
sudo  yum update -y
 ```
 2. Install java and conform it.
 ```
 sudo yum install java-1.8.0 -y
 java -version
 ```
3. Download latest Jenkins code package.

```
sudo yum install wget -y
sudo wget -O /etc/yum.repos.d/jenkins.repo http://pkg.jenkins-ci.org/redhat/jenkins.repo
```
4. Import a key file from Jenkins-CI to enable installation from the package.
```
sudo rpm --import https://pkg.jenkins.io/debian-stable/jenkins.io.key 
```
5. Now install jenkins
```
sudo yum install jenkins -y
```
6. Strat jenkins services
```
sudo systemctl start jenkins
```
7. Check jnekins status
```
sudo systemctl status jenkins
```
8. Access Jenkins server using the public ip of your ec2 on default port no. 8080
```
https://{public_ip}:8080
```
