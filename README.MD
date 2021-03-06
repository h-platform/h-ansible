###Install Ansilble

```
sudo apt-get update
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible

sudo apt-get update
sudo apt-get install ansible
```

Ref: https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-ansible-on-ubuntu-14-04

###Install Roles
```
ansible-galaxy install -r roles.yml
```


###Configuring Ansible Hosts
sudo nano /etc/ansible/hosts

```
[hosts]
host-01 ansible_ssh_host=127.0.0.1 ansible_ssh_user='vagrant' ansible_sudo_pass='vagrant'
```

###Ping
```
ansible -m ping host-01
ansible -m shell -a 'free -m' host-01
```

###Deploy
```
ansible-playbook -v -skK server.yml
```