###Install Ansilble

'''
sudo apt-get update
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible

sudo apt-get update
sudo apt-get install ansible

ansible-playbook -v -skK server.yml
'''

Ref: https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-ansible-on-ubuntu-14-04

###Configuring Ansible Hosts
sudo nano /etc/ansible/hosts

'''
[hosts]
host-01 ansible_ssh_host=127.0.0.1 ansible_ssh_user='vagrant' ansible_sudo_pass='123456'
'''

###Ping
ansible -m ping all
ansible -m ping host-01
ansible -m shell -a 'free -m' host1