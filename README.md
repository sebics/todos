The playbook was tested against a virtual machine Ubuntu 20.04 workstation downloaded from OSBoxes.org

On the Ansible Controller:
configure the inventory.txt with the credentials for the Ubuntu target.
choose a port where the application should run

before running the playbook, use ssh to connect to the ubuntu workstation one time, to update the ssh .known_hosts and avoid that ansible is being stopped.

Clone this repository with:
git clone https://github.com/sebics/todos.git

Start the ansible playbook:
ansible-playbook playbookRunTodos.yml -i inventory.txt --ask-become-pass

