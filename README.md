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