# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
# https://docs.vagrantup.com.

Vagrant.configure('2') do |config|
  config.vm.box = 'mybox'
  config.ssh.insert_key = false


  config.vm.provider :virtualbox do |v|
    v.memory = 256
  end

  config.vm.define :web1 do |web1|
    web1.vm.network :forwarded_port, guest:80, host: 8080
  end
  
  config.vm.define :web2 do |web2|
    web2.vm.network :forwarded_port, guest:80, host: 8081
  end
  
  config.vm.define :db do |db|
    db.vm.network :forwarded_port, guest:80, host: 8082
  end

  config.vm.provision :ansible do |ans|
    ans.playbook = 'provisioning/playbook.yml'
  end
