## {{ cookiecutter.project_title }}

**Installs {{ cookiecutter.project_title }} in a standalone Vagrant box ([debian/buster64](https://app.vagrantup.com/debian/boxes/buster64)), though the use of Ansible (2.10) playbook**


Requirements to run box:
* [Git](https://git-scm.com/downloads)
* [Vagrant](https://www.vagrantup.com/downloads.html)
* [VirtualBox](https://www.virtualbox.org/wiki/Downloads)


## Run

Run the following steps in Terminal (Linux/macOS) or Git Bash (Windows):
```bash
cd {{ cookiecutter.box_name }}
vagrant up
```

After installation process has finished, {{ cookiecutter.project_title }} will be running at 
* {{ cookiecutter.box_ip }}

`vagrant up` creates a new Vagrant box and runs the Ansible  playbook

`vagrant reload --provision` restarting the Vagrant box and re-runs the Ansible playbook 

`vagrant provision` re-runs the Ansible playbook without restarting VM

`vagrant ssh` allows to sshing into the Vagrant box

`vagrant halt`  shuts down the vagrant

`vagrant suspend` saves the state of the Vagrant box and suspends it

`vagrant resume` resumes the Vagrant box from its saved state


## Box source structure & files
* *Vagrant box configuration file*: [Vagrantfile](./Vagrantfile)  
* *Ansible invetory file* for the Vagrant box: [host_vagrant.yml](./host_vagrant.yml)
* *Ansible configuration *file: [ansible.cfg](./ansible.cfg)
* *Ansible entry playbook*: [ansible/playbook.yml](./ansible/playbook.yml)
* *Ansible roles* directory: [ansible/roles](./ansible/roles) --> create 0_hello_playbook role
* *Ansible roles/collections requirements*: [ansible/requirements.yml](./ansible/requirements.yml)

