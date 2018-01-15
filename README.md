# Vagrant

Vagrant is a tool for building and managing virtual machine environments in a single workflow.

## Commands

### Vagrant init

`vagrant init [name [url]]`

This initializes the current directory to be a Vagrant environment by creating an initial Vagrantfile if one does not already exist.

If a first argument is given, it will prepopulate the config.vm.box setting in the created Vagrantfile.

If a second argument is given, it will prepopulate the config.vm.box_url setting in the created Vagrantfile.

`$ vagrant init hashicorp/precise64`  Create a base Vagrantfile
`$ vagrant init -m hashicorp/precise64`  Create a minimal Vagrantfile (no comments or helpers)
`$ vagrant init -f hashicorp/precise64`  Create a new Vagrantfile, overwriting the one at the current path
`$ vagrant init my-company-box https://boxes.company.com/my-company.box` Create a Vagrantfile with the specific box, from the specific box URL
`$ vagrant init --box-version '> 0.1.5' hashcorp/precise64`  Create a Vagrantfile, locking the box to a version constraint

### Vagrant up

`vagrant up [name|id]`

This command creates and configures guest machines according to your Vagrantfile.

### Vagrant status

`vagrant status [name|id]`

This will tell you the state of the machines Vagrant is managing.

### Vagrant destroy

`vagrant destroy [name|id]`

This command stops the running machine Vagrant is managing and destroys all resources that were created during the machine creation process.

### Vagrant halt

`vagrant halt [name|id]`

This command shuts down the running machine Vagrant is managing.

### Vagrant reload

`vagrant reload [name|id]`

The equivalent of running a halt followed by an up.

### Vagrant suspend

`vagrant suspend [name|id]`

This suspends the guest machine Vagrant is managing, rather than fully shutting it down or destroying it.

### Vagrant resume

`vagrant resume [name|id]`

This resumes a Vagrant managed machine that was previously suspended, perhaps with the suspend command.

### Vagrant ssh

`vagrant ssh [name|id] [-- extra_ssh_args]`

This will SSH into a running Vagrant machine and give you access to a shell.

### Vagrant ssh-config

`vagrant ssh-config [name|id]`

This will output valid configuration for an SSH config file to SSH into the running Vagrant machine from ssh directly (instead of using vagrant ssh).



Reference: https://www.vagrantup.com/docs
