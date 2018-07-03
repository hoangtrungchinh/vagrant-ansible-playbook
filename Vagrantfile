Vagrant.configure('2') do |config|
  config.vm.box = 'bento/ubuntu-16.04'
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
end
