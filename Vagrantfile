# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "geerlingguy/centos7"

  config.ssh.insert_key = false

  config.vm.synced_folder ".", "/vagrant", disabled: true

  config.vm.provider :virtualbox do |v|
      v.memory = 2048 # 2GB
      v.linked_clone = true
  end

  config.vm.define "es1" do |es|
    es.vm.hostname = "es1-orc"
    es.vm.network :private_network, ip: "192.168.60.2"
  end

  config.vm.define "es2" do |es|
    es.vm.hostname = "es2-orc"
    es.vm.network :private_network, ip: "192.168.60.3"
  end

  config.vm.define "es3" do |es|
    es.vm.hostname = "es3-orc"
    es.vm.network :private_network, ip: "192.168.60.4"
  end

  config.vm.define "kibana" do |es|
    es.vm.hostname = "kibana-orc"
    es.vm.network :private_network, ip: "192.168.60.5"
  end

end
