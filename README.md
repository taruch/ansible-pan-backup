# ansible-pan-backup

This will backup a panos firewall to a repo. This should be an internal repo, because you don't really want to share your firewall configuration with the world.

## Getting started

https://pan.dev/ansible/docs/panos/tutorials/setup/

You will need to add a group_vars directory, and create in a group file for your firewalls.

Example: group_vars/panos_fw

provider:
  ip_address: "{{ ansible_host }}"
  password: < put your password here - you should really vault this >
  username: < put your username here >
git_url: < put your git ssh clone url here >