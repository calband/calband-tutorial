# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    config.vm.provider "virtualbox" do |v|
        # Change if needed
        v.customize ["modifyvm", :id, "--memory", "2048"]
    end

    # Cal Band VM
    config.vm.box = "calband/xenial64v1"
    config.vm.box_url = "https://s3-us-west-1.amazonaws.com/calband-virtualboxes/xenial64v1.box"
    
    # Forward a port from the guest to the host, which allows us to access the ports
    # exposed by the VM from our local machine.
    config.vm.network :forwarded_port, guest: 8000, host: 8000
    
    # sync the current directory with the /vagrant directory on the virtual machine
    config.vm.synced_folder ".", "/vagrant", :mount_options => ["fmode=666"]

    # Enable provisioning using Ansible
    config.vm.provision "ansible_local" do |ansible|
        ansible.playbook = "vagrant/playbook.yml"
        ansible.become = true
    end
end
