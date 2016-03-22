# provision-vm
Ansible Playbook for my basic vm setup

```
useradd deploy
passwd deploy
mkdir /home/deploy
mkdir /home/deploy/.ssh
chmod 700 /home/deploy/.ssh
nano /home/deploy/.ssh/authorized_keys
chmod 400 /home/deploy/.ssh/authorized_keys
chown deploy:deploy /home/deploy -R
echo 'deploy ALL=(ALL) NOPASSWD: ALL' > /etc/sudoers.d/deploy
```

Edit vars/defaults.yml!

```ansible-playbook playbook.yml -i "<ip address>"```
