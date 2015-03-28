# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure('2') do |config|
    config.vm.box = 'ubuntu/trusty64'
    config.vm.hostname = 'weirdmeetup'

    config.vm.network :forwarded_port, guest: 3000, host: 3000
    config.vm.network :private_network, ip: "192.168.33.11"
    config.vm.synced_folder ".", "/home/vagrant/server"
    config.vm.provision :shell, path: 'bootstrap.sh', keep_color: true
end
