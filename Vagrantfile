# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    config.vm.provider "virtualbox" do |v|
        # Change if needed
        v.customize ["modifyvm", :id, "--memory", "2048"]
    end

    # Cal Band VM
    config.vm.box = "calband/bionic64"
    
    # Forward a port from the guest to the host, which allows us to access the ports
    # exposed by the VM from our local machine.
    config.vm.network :forwarded_port, guest: 8000, host: 8000
    
    # sync the current directory with the /vagrant directory on the virtual machine
    config.vm.synced_folder ".", "/vagrant", :mount_options => ["fmode=666"]
end
