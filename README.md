# ansible-config-mgt
for ansible use 
timmy is fed up of akure
remmy no dy use 

HI

we are on project 14

# INSTALL AND CONFIGURE JENKINS SERVER

Step 1 – Install Jenkins server

Create an AWS EC2 server based on Ubuntu Server 20.04 LTS and name it "Jenkins"

Install JDK (since Jenkins is a Java-based application)

sudo apt update

sudo apt install default-jdk-headless

# Install Jenkins

wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -

sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > \
    /etc/apt/sources.list.d/jenkins.list'

sudo apt update

sudo apt-get install jenkins

and i make sure Jenkins is up and running

sudo systemctl status jenkins




##### Running Ansible Playbook fronm Jenkins
Install ansible in Jenkins sudo apt install ansible and ansible plugin in Jenkins UI. We need to install some dependencies for ansible to work properly, since we have some ansible modules in the roles. This will allow ansible playbook to run properly.

yum install python3 python3-pip wget unzip git -y

python3 -m pip install --upgrade setuptools

python3 -m pip install --upgrade pip

python3 -m pip install PyMySQL

python3 -m pip install mysql-connector-python

python3 -m pip install psycopg2==2.7.5 --ignore-installed

ansible-galaxy collection install community.mysql

ansible-galaxy collection install community.postgresql

ansible-galaxy collection install community.general




# jenkins plugins installed 
Ansible plugin

Blue ocean

Strict Crumb Issuer Plugin


Run Condition Plugin

Fast Track Queue Optimizer


ansiblePlaybook credentialsId: 'private-key', installation: 'ansible', inventory: 'inventory/dev', playbook: 'playbooks/site.yml'


# How to install jfrog aertifactory

ansible-galaxy collection install jfrog.platform


Verify that you reference the Ansible Collection in your playbook when using these roles.

---
- hosts: artifactory_servers
      collections:
        - jfrog.platform
      roles:
        - artifactory
####  STEPS TAKEN AFTER INSTALLIMG JFROG ARTIFACTORY

Change the security group
then the ip-address:8081
username: Admin
password: password

change the password after logging in the jfrog 

Then create repository 

Create repository -> Select Package Type -> Generic, enter Repository Key as PBL, save and finish.

Then after the configuration in jenkins for the Jfrog 

 first all fork then 

You clone https://github.com/Timmyzooto01/php-todo.git todo-php to your project then create a jenkinsfile along side with it 

##### composer 

https://www.how2shout.com/linux/how-to-install-composer-on-ubuntu-22-04-20-04-lts/

curl -sS https://getcomposer.org/installer -o composer-setup.php

sudo mv composer-setup.php /usr/bin/composer

#### Creating another database and user 

# Databases.
mysql_databases:
   - name: Homestead
     collation: utf8_general_ci
     encoding: utf8
     replicate: 1

# Users.
mysql_users: 
  - name: 'Homestead'
    host: 172.31.21.41 (jenkins-ansible server)
    password: secret
    priv: '*.*:ALL,GRANT'


then 
we launch our windows terminal and connect to the database to be sure of the database we created to be there 

so only my database was creating and decided to login the instance and create a user according to the project 
Create database homestead;
CREATE USER 'homestead'@'jenkins-server-ip' IDENTIFIED BY 'sePret^i';
GRANT ALL PRIVILEGES ON * . * TO 'homestead'@'jenkins-servre -ip';

To confirm 
sudo mysql 
show databases;
select user, host from mysql.user;


to the next step 
then install 
sudo apt install mysql-client in your jenkins-server instnace 
restart the mysql after 
#



We added 
DB_CONNECTION=mysql
DB_PORT=3306
 to the .env.sample file 
 input the database ip address to the file also 


Then connect to your database from the jenkins 



Bundle the application code for into an artifact (archived package) upload to Artifactory, 

but ensure you install zip `sudo apt install zip -y.`

 
You can only deploy to artifactory, if a unit test has been done on it. Publish the result artifact into Artifactory.


update the necessary things on the task from the artifactory 


then check your todo ip-address to confirm your deployment as well too 


Configure SonarQube
Software Quality - The degree to which a software component, system or process meets specified requirements based on user needs and expectations.

Software Quality Gates - Quality gates are basically acceptance criteria which are usually presented as a set of predefined quality criteria that a software development project must meet in order to proceed from one stage of its lifecycle to the next one.


ansible-galaxy install lrk.sonarqube

cd roles/


mv lrk.sonarqube sonarqube



###----- sonarqude property 

i added this to the properties 

## Flex Specific Properties

# retrieve code coverage data from the Cobertura report
sonar.flex.cobertura.reportPath=coverage-report/coverage-cobertua-flex.xml



# PL/I Specific Properties
sonar.pli.marginLeft=2
sonar.pli.marginRight=0



