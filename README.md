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


You clone https://github.com/darey-devops/php-todo.git todo-php to your project then create a jenkinsfile along side with it 
