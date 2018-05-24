# openerp-deploy
Vagrant & Ansible project to deploy OpenERP server

# Requirements
Install following packages:
`apt install ansible ansible-playbook vagrant`

# Configure
Make your own variables.yml, use variables_example.yml as example

# Run
Run `vagrant up`
Go into erpserver `vagrant ssh erpserver`

To run Ansible without Vagrant, run as a root: `ansible-playbook erpdeploy.yml`
