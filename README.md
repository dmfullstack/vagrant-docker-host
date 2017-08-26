# vagrant-docker-host

Clone the repository and then type:

`vagrant up`

Once the provisioning of the virtual machine has been completed, then simply type the below to access the host and run Docker commands:

`vagrant ssh`

`sudo su -`

`docker info`

The above will confirm that Docker is installed and usable.   

Note: if you get an error like: `docker: Error response from daemon: devmapper: Error activating devmapper device for`, then reboot the Vagrant virtual machine and that seems to resolve the issue.
