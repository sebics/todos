_To run_ on the Ansible Controller:

Clone this repository with:

    git clone https://github.com/sebics/todos.git


Configure the VM target4 name and IP in the inventory.txt Choose the listening port for the application in the inventory.txt

Start the ansible playbook:

    ansible-playbook playbookRunTodos.yml -i inventory.txt --ask-become-pass
    or
    ansible-playbook playbook_create_app_user.yaml  -i inventory.txt --ask-become-pass 

Password for the sudo on the target VM needs to be entered when requested at command prompt.

Link to the video of the application running on vimeo: https://vimeo.com/748314812

_Pre-requisites_:

This playbook was tested agains an Ubuntu 20.04 VM image downloaded from osboxes.org
Before running the ansible playbook few things: start the ubuntu image file, use ssh to connect one time from the Ansible controller to the Ubuntu workstation (user/pass osboxes/osboxes.org) to update the ssh .known_hosts with the target machine ssh key and avoid that ansible gets stopped. Also on the target machine modify hostname in /etc/hosts and /etc/hostnames to be target4.

As the playbook takes around 30 minutes long to install the packages in my environment, some progress of installation can be checked on the target machine by tail -f /var/log/apt/term.log
