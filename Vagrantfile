# -*- mode: ruby -*-
# vi: set ft=ruby :

machines = [
  {"name" => "redis-cluster-1", "ip" => "192.168.33.10"},
  {"name" => "redis-cluster-2", "ip" => "192.168.33.11"},
  {"name" => "redis-cluster-3", "ip" => "192.168.33.12"},
]

Vagrant.configure("2") do |config|

  machines.each do |machine|
    config.vm.define machine["name"] do |vm_config|
      vm_config.vm.box = "ubuntu/focal64"
      vm_config.vm.network "private_network", ip: machine["ip"]
  
      vm_config.vm.provider "virtualbox" do |v|
        v.name = machine["name"]
      end
    end
  end
end
