
# Prometheus workshop

These are Ansible playbooks used to setup *Prometheus 101* workshop.


## How to run at workshop site

 * Run some CentOS 7 hosts. 
 * Apply the playbook to the hosts.
 
## How to run at home

 * Setup [Vagrant][vagrant] on your machine 
 * Run `vagrant up`
 * Open to `http://192.168.33.11/`. 
 * Login with ssh using `vagrant ssh`
 
 * Use `vagrant destroy` to clean up the virtual machines.
 
The address can be changed in `Vagrantfile`.
 

## License

CC-0
 
[vagrant]: https://www.vagrantup.com/docs/installation/
