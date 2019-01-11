# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

	config.vm.define "app1" do |app|
		app.vm.box = "mvbcoding/awslinux"
		app.vm.hostname = "orc.app1.dev"
		app.vm.network "private_network", ip: "192.168.60.4"
		app.vm.network "forwarded_port", guest: 80, host: 8080
  	app.vm.network "forwarded_port", guest: 443, host: 8443
	end

	config.vm.define "db" do |db|
		db.vm.box = "ubuntu/trusty64"
		db.vm.hostname = "org.db.dev"
		db.vm.network "private_network", ip: "192.168.60.5"
	end
	# config.vm.box = "centos/7"
	 # config.vm.customize ["modifyvm", :id, "--audio", "none"]
	# Create a private network, which allows host-only access to the machine
	# using a specific IP.
	# config.vm.provider :virtualbox do |vb|
	# 	vb.memory = 2048
	# 	vb.cpus = 2
	# end
	# config.vm.provision "shell", inline: "sudo yum -y update"

end
