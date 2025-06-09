java --version
sudo apt update
sudo apt install jenkins -y
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
goto jenkins create pipeline and build
mvn archetype:generate
cd maven folder name
ls
nano pom.xml
mvn package
ls target/*.jar
readlink -f target/*.jar
nano deployyart.yml
---

- name: Deploy artifact built by jenkins
  hosts: localhost
  become: true
  tasks:
    - name: copy JAR to deployment folder
      copy:
       src: path which we get in redlink
       dest: /opt/deploy/maven folder.jar
       ansible-plyabook deployyart.yml --ask-become-pass


7th
sudo adduser username
sudo usermod -aG sudo username
sudo su -veer
sudo apt update && sudo apt ansible
ansible --version
sudo mkdir -p /etc/ansible
sudo nano /etc/ansible/hosts
ansible all -m ping
nano playbook.yml
---
- name: basic hello world
  hosts: all
  tasks:
   - name:print hello world
     debug:
       msg: "hello world"
 ansible-playbook playbook.yml    
