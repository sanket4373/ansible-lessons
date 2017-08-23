- Each ansible command has both the content of the change you want to run against with the ansible tool you have the ability to specify all your potential targets (hosts/machines) in advance

- with ansible you have put your target host in advance

#### Inventory

- Static: a static file that has a list of hosts
- Dynamic: which is normally implemented as a script that then calls some other API or service to populate all the host information and variable data


- Create a inventory file to populate the list of nodes inside it

- Here, I have created a directory called `ansible` inside my control node and created a inventory file named `hosts`. The path is:  `/vagrant/work/ansible/hosts`

- To list the inventory file you will have to pass it. The ansible cli command to do that is:

  `$ ansible -i hosts --list-hosts all`

 ```[WARNING]: Found both group and host with same name: control

  hosts (5):
    control
    db01
    app01
    app02
    lb01
```

- Precedence that ansible follows to look for the list of nodes is by default `/etc/ansible/hosts` if the hosts are not provided in any other inventory information and that's set by the global ansible configuration `/etc/ansible/ansible.cfg`.

- This can be overridden by putting a configuration file in our local directory

- I have created a file named `ansible.cfg` and have put the name of the host file inside it. This overrides the `.cfg` file which is inside `/etc/ansible/ansible.cfg`

- Now we don't have to mention the `-i` and the name of the `hosts` file exclusively in the command to list the host names.

  `$ ansible --list-hosts all`


- Listing specific hosts selection

  `$ ansible  --list-hosts <name_of_the_host>`

- Command to ping all hosts to test their connectivity

  `$ ansible -m ping all` 
