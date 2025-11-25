# nginx-imp

### ec2 instance eu-west-2 region- Install Jenkins inside this instance
```
 sudo apt update -y
    2 sudo apt update
    3  sudo apt install fontconfig openjdk-21-jre
    4  sudo wget -O /etc/apt/keyrings/jenkins-keyring.asc   https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
    5  echo "deb [signed-by=/etc/apt/keyrings/jenkins-keyring.asc]"   https://pkg.jenkins.io/debian-stable binary/ | sudo tee   /etc/apt/sources.list.d/jenkins.list > /dev/null
    6  sudo apt update
    7  sudo apt install jenkins
    8  sudo cat /var/lib/jenkins/secrets/initialAdminPassword
    9  which git
```
### install AWS cli boto Ansible terraform on the Jenkins Server
### https://github.com/Gagan543-ui/Nginx-one-click-automation.git -call the repo in this jenkins pipeline job with
AWS credential-- (jenkinsdemo) id  Manually Added where we are storing the Access key and Secret key 

### Building the above the Job using git hub jenkins file to create one click infra of Nginx
### Download the pem key file from the jenkins workspace to the local machine 
check the Permission of the Downloaded file and the just add read for the user 
```
ls -la ./nginx-demo-key.pem #to check permission

chmod 400 nginx-demo-key.pem

ls -la ./nginx-demo-key.pem # to varify 
```
### ssh to bastion from local 

### Copy the identity file local to bastion

```
scp -i nginx-demo-key.pem ~/.ssh/nginx-demo-key.pem ubuntu@public_ip:~/
```
### ssh to bastion 
### ssh to nginx(Private Instance)
```
sudo systemctl status nginx
```
```
curl http://localhost:80
```




