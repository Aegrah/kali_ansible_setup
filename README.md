# Kali Linux quick setup through an Ansible Playbook
This is my personal Kali Linux setup that I install as a base for my new Kali Linux images. The only package required to get it up and running is ansible. 

This repository is constantly being updated with new packages and configurations. It can be used as a template to set up your own prefered Kali Linux installation. 

## How to run
Install Ansible as prerequisite, then run the ansible-playbook command and wait. 
```sh
sudo apt install ansible -y
sudo ansible-playbook kali-setup.yml
```

## Possible issues
The playbook clones different Github repositories and downloads several release files from dynamic GitHub release pages. It's possible that one of the files is no longer available or that the location has changed. If it errors out, just change the URL's to the new correct file location. 
