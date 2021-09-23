# Cookie cutter for creating Vagrant boxes
Python [cookiecutter](https://cookiecutter.readthedocs.io) library allows for the creation of project structures from templates.

This repository uses [cookiecutter](https://cookiecutter.readthedocs.io) to create the structure and essential file to create Vagrant boxes, where a given software setup is automated with Ansible.

## Running cookie cutter - to create Vagrant box file structure
* clone repo: `git clone https://github.com/TIBHannover/cookiecutter-for-vagrant-boxes.git`
* `cd cookiecutter-for-vagrant-boxes` 
* create a local python3 virtual environment
* install [cookiecutter](https://cookiecutter.readthedocs.io) python library `pip install cocookiecutter`
* go to the parent directory: `cd ..` 
* run the cookiecutter: `cookiecutter cookiecutter-for-vagrant-boxes` to create a new instance from the cookiecutter
* provide the appropriate values to the questions asked
* go into the created folder, which will have the same name as the box name: `cd {{ cookiecutter.box_name }}`
* see the [{{ cookiecutter.box_name }}/README.md]({{ cookiecutter.box_name }}/README.md) for further info on the box source code directory structure
* start vagrant box `vagrant up` - for testing purposes
* started editing away the playbook


