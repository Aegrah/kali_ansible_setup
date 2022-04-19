# Kali Linux Ansible Playbook setup
This is my personal Kali Linux setup that I install as a base for my fresh Kali Linux images. The only package required to get it up and running is ansible. 

This repository is constantly being updated with new packages and configurations. It can be used as a template to set up your own prefered Kali Linux installation. 

## How it looks
The Ansible script uses the powerlevel10k zsh theme in combination with the nord-tmux theme by arcticicestudio. The ls command is replaced by exa to get more color and detail in file listings. A screenshot of the themed setup is shown below.

![customized_kali](https://user-images.githubusercontent.com/78494512/164030779-f74e7387-c3ef-4984-9722-9629519c0a11.png)

If you would like a similar setup, then read along!

## How to run
Install Ansible as prerequisite, then run the ansible-playbook command and wait. 
```sh
sudo apt install ansible -y
sudo ansible-playbook kali-setup.yml
```
## Post configuration
After the playbook has finished, I would recommend rebooting the system and launching a zsh session. You will be prompted to configure the zsh terminal to your preference. If you want to redo the configuration you can always reinitialize the configuration menu.
```sh
p10k configure
```
You will have to configure both a root and a regular user terminal. 

After configuring the terminal, launch a tmux session and install the themes and plugins that were applied during the configuration through the ctrl + b + I (capital i) hotkey. 

## Possible issues
The playbook clones different Github repositories and downloads several release files from dynamic GitHub release pages. It's possible that one of the files is no longer available or that the location has changed. If it errors out, just change the URL's to the new correct file location. I added some additional error handling so it will not break the script. 
