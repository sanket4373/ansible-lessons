### PlayBooks

- Playbook is a file written in `yaml` syntax made up of plays and a play is simply a set of target hosts and the tasks to execute them against the target hosts.

- Inside the `yaml` file there are two keys :
  1. `hosts: all` - we are setting this key with a value all since we want to run this play on all the host nodes.
  2. `tasks:` This can a list of tasks/commands which needs to executed.

**Note:**  A play is a way to build multiple tasks that execute against the same target in a sequential order as pet the tasks written inside the playbook.
