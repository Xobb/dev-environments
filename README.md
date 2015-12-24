dev-environments
================

This repository is intended to store configurations for different virtual development (or other) environments.

You could push here any configuration for such environment if you think it will be useful to other community members.

Vagrant up
==========

As we store the Vagrant file in this repository and the project in another repository you will have to update the ```Vagrantfile``` yourself.
To do so you will have to find the following line in ```Vagrantfile```:

    config.vm.synced_folder "./", "/vagrant", type: "nfs"
    
which is usually in the end of the file and update the first argument to be the relative path to your project. Example:

    config.vm.synced_folder "../oro-project", "/vagrant", type: "nfs"

After you set up the path you will have to launch the instance with the following command:

    vagrant up
    
This configuration has been tested on OSX El Capitan. When reporting issues, please specify your OS.
