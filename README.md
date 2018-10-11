# elk_centos7

This script install stack ELK on centos7 

N.B.

Oracle Jdk it is not installed. The user will have to install it through rpm package or tar.gz ans afterwards setting JAVA_HOME


However this installation is tested with Oracle Jdk 1.8.0_181
JAVA_HOME has been set in /usr/java/jdk1.8.0_181-amd64


To install stack ELK on centos7 run:

ansible-playbook -i hosts site.yaml

To uninstall stack ELK on centos7 run:

ansible-playbook -i hosts deprovision.yaml

Adding Tags to permit run only specific task of playbook

Tags:

upgrade
elasticsearch
logstash
kibana
ntp


For example, to launch only task regarding upgrade os, run:
 
ansible-playbook -vv --tags "upgrade" -i hosts site.yaml
