# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
 
#konfigurasi box untuk sistem operasi debian jessie 64bit
 	 config.vm.box = "debian/jessie64"
 	 config.vm.provider "virtualbox" do |vb|
  	vb.name = "ujian"
#konfigurasi virtual box ram 1GB cpu 1 core
  	vb.memory = "1024"
	vb.cpus = "1"
#konfigurasi provisioning
 config.vm.provision "shell", path: "install.sh"

#konfigurasi network 
#port forwarding
  config.vm.network "private_network", ip: "192.168.2.22"

  config.vm.network "forwarded_port", guest: 80, host: 8000
end
  end
