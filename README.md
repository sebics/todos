The playbook was tested against a virtual machine Ubuntu 20.04 workstation downloaded from OSBoxes.org

On the Ansible Controller:

Clone this repository with:

    git clone https://github.com/sebics/todos.git

_To run_:

Configure the VM name and IP in the inventory.txt

Choose a port for the application in the inventory.txt

Start the ansible playbook:

    ansible-playbook playbookRunTodos.yml -i inventory.txt --ask-become-pass

Password for the sudo is asked at command prompt.

Link to the video of the application running on vimeo: https://vimeo.com/748314812

_Pre-requisites_:

Before running the ansible playbook few things: start the ubuntu image file, use ssh to connect one time from the Ansible controller to the Ubuntu workstation (user/pass osboxes/osboxes.org) to update the ssh .known_hosts with the target machine ssh key and avoid that ansible gets stopped. Also on the target machine modify hostname in /etc/hosts and /etc/hostnames to be target4.

As the playbook takes around 30 minutes long on my machine to install the packages, some progress of installation can be checked on the target machine by tail -f /var/log/apt/term.log
