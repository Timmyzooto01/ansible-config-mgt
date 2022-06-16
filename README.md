# ansible-config-mgt
for ansible use 
timmy is fed up of akure
remmy no dy use 




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

#### Craeting anlother database and user 

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
we launch our windows terminal and connevct to the database to be sure of the database we created to be there 

so only my database was creating and decided to login the instance and create a user according to the project 
Create database homestead;
CREATE USER 'homestead'@'jenkins-server-ip' IDENTIFIED BY 'sePret^i';
GRANT ALL PRIVILEGES ON * . * TO 'homestead'@'jenkins-servre -ip';

To confirm 
sudo mysql 
show databases;
select user, host from mysql.user;


to the next step 






