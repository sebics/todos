The playbook was tested against a virtual machine Ubuntu 20.04 workstation downloaded from OSBoxes.org

On the Ansible Controller:

Clone this repository with:

    git clone https://github.com/sebics/todos.git

Configure the inventory.txt with the credentials for the Ubuntu target, and choose a port where the application should run

Before running the ansible playbook, use ssh to connect to the ubuntu workstation one time, to update the ssh .known_hosts with the target ssh key and avoid that ansible gets stopped.

Start the ansible playbook:

    ansible-playbook playbookRunTodos.yml -i inventory.txt --ask-become-pass

Link to the video of the application running on vimeo: https://vimeo.com/748314981
