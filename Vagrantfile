# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

	config.omnibus.chef_version = :latest
	config.berkshelf.enabled = true

  config.vm.box = "opscode-precise64-provisionerless"

  config.vm.box_url = "https://opscode-vm-bento.s3.amazonaws.com/vagrant/opscode_ubuntu-12.04_provisionerless.box"

	config.vm.network :private_network, ip: "172.16.30.50"

	config.vm.provision :chef_solo do |chef|
		chef.add_recipe "deployd"
	end

end
