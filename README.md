# Ansible Playbook for Sonarqube
An Ansible playbook to run Sonarqube as a docker container on a VM built with Vagrant

## Commands
* vagrant up
* vagrant ssh-config > .sshconfig
* ssh -F .sshconfig default
* ansible-playbook --private-key .vagrant/machines/default/virtualbox/private_key -u vagrant -i hosts playbook.yml

Just to check ssh parameters that vagrant uses
`vagrant ssh-config | awk 'NR>1 {print " -o "$1"="$2}'`
To ssh:
`ssh $(vagrant ssh-config | awk 'NR>1 {print " -o "$1"="$2}') localhost`

