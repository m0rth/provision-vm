## provision-vm
A Ansible Playbook for my basic vm setup

TODO: what does the playbook install and change?
#### Prerequisites
A VPS or baremetal Server with Ubuntu 14.04 LTS or Debian Jessie

Create a privileged User named `deploy` and add a SSH Key to enable passwordless SSH Login:

```
useradd deploy
passwd deploy
mkdir /home/deploy
mkdir /home/deploy/.ssh
chmod 700 /home/deploy/.ssh
nano /home/deploy/.ssh/authorized_keys # << copy ssh key here
chmod 400 /home/deploy/.ssh/authorized_keys
chown deploy:deploy /home/deploy -R
echo 'deploy ALL=(ALL) NOPASSWD: ALL' > /etc/sudoers.d/deploy
```

Edit `vars/user.yml` to your liking.

Run the playbook:

```ansible-playbook playbook.yml -i "13.37.4.20, "```

Replace `13.37.4.20` withe the IP or FQDN of your target machine.

You can add `-vv` to the Ansible command to get a more verbose output!

If you only want to reapply or change the configuration add `--tags config` to the command.
