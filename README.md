# sbsc-ansible

An Ansible script for provisioning a RaspberryPi to run [sbsc](https://github.com/majellatech/sbsc) on boot.

## Instructions

0. Set the `ansible_host` variable in `hosts`
1. Write Raspberry Pi OS to SD card
2. Mount it and `touch /boot/ssh`
3. Boot RPi and make sure it's connected to the network
4. Run `ssh pi@[ip-here]` to add the RPi to the SSH known hosts
5. Run `ansible-playbook -i hosts setup-role.yml`
6. Add `channel_id` (from parish channel URL) and `api_key` (from https://console.cloud.google.com/apis/api/youtube.googleapis.com/credentials) to `sbsc.py`
7. Reboot
