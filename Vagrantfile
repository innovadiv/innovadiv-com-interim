# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  
  config.ssh.shell = "bash -c 'BASH_ENV=/etc/profile exec bash'"
  config.vm.box = "precise64"
  config.vm.box_url = "http://files.vagrantup.com/precise64.box"
  config.vm.provision "shell", path: "tools/vagrant.sh"
  config.vm.network "forwarded_port", host: 9112, guest: 80
  config.vm.provision "shell", path: "tools/start-instance.sh", run: "always"

end