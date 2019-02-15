# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # create vm1
  config.vm.define :vm1 do |vm1_config|
      vm1_config.vm.box = "centos/7"
      vm1_config.vm.hostname = "vm1"
      vm1_config.vm.network :private_network, ip: "10.0.15.11"
      vm1_config.vm.provider "virtualbox" do |vb|
        vb.memory = "512"
        vb.cpus = 1
      end
      #mgmt_config.vm.provision :shell, path: "bootstrap-mgmt.sh"
  end

  # create vm2
  config.vm.define :vm2 do |vm2_config|
      vm2_config.vm.box = "centos/7"
      vm2_config.vm.hostname = "vm2"
      vm2_config.vm.network :private_network, ip: "10.0.15.12"
      vm2_config.vm.provider "virtualbox" do |vb|
        vb.memory = "512"
        vb.cpus = 1
      end
  end

  # create vm3
  config.vm.define :vm3 do |vm3_config|
      vm3_config.vm.box = "centos/7"
      vm3_config.vm.hostname = "vm3"
      vm3_config.vm.network :private_network, ip: "10.0.15.13"
      vm3_config.vm.provider "virtualbox" do |vb|
        vb.memory = "512"
        vb.cpus = 1
      end
  end
end


#   # create some web servers using loop
#   # https://docs.vagrantup.com/v2/vagrantfile/tips.html
#   (1..2).each do |i|
#     config.vm.define "web#{i}" do |node|
#         node.vm.box = "centos/7"
#         node.vm.hostname = "web#{i}"
#         node.vm.network :private_network, ip: "10.0.15.2#{i}"
#         node.vm.network "forwarded_port", guest: 80, host: "808#{i}"
#         node.vm.provider "virtualbox" do |vb|
#           vb.memory = "512"
#         end
#     end
#   end
# end
