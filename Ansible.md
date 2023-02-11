

# Installations

```
 sudo apt update
 sudo apt-add-repository ppa:ansible/ansible
 sudo apt update
 sudo apt install ansible

```

# Verify Instllations


```
 cat /etc/ansible/hosts
 
```


# local to virtual machine

```
 scp -i "ansible-all-access-key.pem" ansible-all-access-key.pem ubuntu@ec2-44-201-8-225.compute-1.amazonaws.com:/home/ubuntu/.ssh

```


# Virtual machine to local 
```
scp -i "ansible-all-access-key.pem" ubuntu@ec2-44-201-8-225.compute-1.amazonaws.com:/home/ubuntu/ansible/date.yml .
```


```

 ansible servers -m ping
 ansible -i prod_inv servers -m ping
 ansible -i /home/ubuntu/ansible/inventories/prod_inv servers -m ping
 ansible -i /etc/ansible/hosts servers -m ping
 
 
ansible servers -a "df -h"
ansible servers -a "uptime"


```



```

ansible 

-m v/s -a


```



# ansible configurations

```


[servers]
server_1 ansible_host=34.20.63.13
server_2 ansible_host=54.209.157.26
server_3 ansible_host=54.17.13.11

[servers:vars]
ansible_python_interpreter=/usr/bin/python3
ansible_ssh_private_key_file=/home/ubuntu/.ssh/ansible-all-access.pem

```
