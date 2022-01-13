# cc-1-folders-overflow

this project contains the following files:
- Vagrantfile: contains configuration for a vm to host our containers.
- playbook.yml: Ansible's playbook, not used directly but set as a provisioner for the Vagrant vm.
- docker-compose: used inside Ansible's playbook to run containers inside Vagrant vm.
- conf.d: directory mounted to openresty container to load nginx/openresty configuration.
- roles: contains Ansible roles for the sake of clean structure.

launching the vm:

    $> vagrant up

tasks:

 - [x] spinning an Openresty container.
 - [x] creating a [lua script](https://github.com/mathematikoi/cc-1-folders-overflow/blob/master/conf.d/default.conf) to reformulate uri from `/stores/XYZ20211008ABC/categorie/image.png` to  `/stores/XY/Z2/XYZ20211008ABC/categorie/image.png`
 - [ ] creating a sample application for testing.
	 - testing using curl:
	 `$> curl <vagrant_vm_ip>:8080/stores/XYZ20211008ABC/categorie/image.png`
