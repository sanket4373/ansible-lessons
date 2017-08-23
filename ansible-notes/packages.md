### Packages


1. **Apt module:** Installing apt packages using Ansible is similar to using CLI to install package on a Linux system

 - `name=nginx state=present update_cache=yes`
 - `name=nginx` is the name of the package we want to install on our target host.
 - `state` and `update_cache` are parameters
 - In `state=present` what `present` does is that it looks on the target host if the package is already installed and if not, it will install the current latest version is. Whereas, `absent` will remove the existing package.
 - `update_cache=yes` this is equivalent to `apt get update` in linux and this command is executed in ansible after the package is installed.
