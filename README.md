# Ansible Raspberry Pi

Ansible RPI Playbooks for learning Ansible. These were playbooks I created while going through the [Ansible Documentation](https://docs.ansible.com/)

## Initial Setup:

1. Edit the `hosts` file in the root directory of this project to use your RPI's IP Address
2. Edit the `ansible.cfg` file in the root directory of this project to use your RPI's remote_user (it is pi by default)
3. Make sure ansible is installed, you can install it via `sudo -H /usr/local/bin/pip3 install ansible`
4. Run the playbook you want to execute via the command below:

```
# View that your host will be executed on
ansible-playbook playbooks/folder/folder.yaml --limit rpi -i ./hosts --list-hosts 

# Execute by removing --list-hosts
ansible-playbook playbooks/folder/folder.yaml --limit rpi -i ./hosts

```

## Playbooks

- [Adding Multiple Files to Remote Hosts](https://github.com/BaReinhard/ansible_rpi/tree/master/playbooks/multiple-files)
- [Check the OS Release Information of each Remote Host](https://github.com/BaReinhard/ansible_rpi/tree/master/playbooks/os-release)
- [Configure Multiple Remote Hosts with a WPA Supplicant File with Updating Wifi Information](https://github.com/BaReinhard/ansible_rpi/tree/master/playbooks/wpa-init)
- [Configure Multiple Remote Hosts with Shairport-Sync](https://github.com/BaReinhard/ansible_rpi/tree/master/playbooks/shairport-sync-setup)
- [Setup an RPI as a Plex Server](https://github.com/BaReinhard/ansible_rpi/tree/master/playbooks/plex)

## Common Errors:

```
# {"msg": "to use the 'ssh' connection type with passwords, you must install the sshpass program"}

# you will need to install sshpass, for mac 
brew install https://raw.githubusercontent.com/kadwanev/bigboybrew/master/Library/Formula/sshpass.rb
```
