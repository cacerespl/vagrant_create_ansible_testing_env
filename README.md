# Using Vagrant for creating an ansible environment for practicing and learning
Use Vagrant to create an environment for practicing and learning ansible, the Vagrantfile will user ansible to provision the environment for you.


This environment will create three servers:

- **ansible_server**: the Ansible control server, an ubuntu machine with an IP address 192.168.100.11
- **server2**: another Ubuntu server with an IP address 192.168.100.22.
- **server3**: a Centos server with an IP address 192.168.100.33.

# To create the environment clone the repository and then run:
vagrant up

After creating the environment, you need do perform the following steps:

- Connect to the ansible_server (**vagrant ssh ansible_server**) and login as ansible (**su - ansible**) with the password **ansible** (already provisioned with ansible by using the ansible_server.yml).
- Copy the keys (already installed) from the **ansible_server** to **server2** and **server3** by issuing **ssh-copy-id ansible@192.168.100.22** and **ssh-copy-id ansible@192.168.100.33**. Both servers (server2 and server3) have already created the user ansible with the password ansible.









