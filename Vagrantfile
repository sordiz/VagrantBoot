# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure('2') do |config|
  config.vm.box      = 'ubuntu/yakkety64' # 16.10
  config.vm.hostname = 'rails-dev-box'

  config.vm.network :forwarded_port, guest: 3000, host: 3000
  config.vm.network :forwarded_port, guest: 9013, host: 9013

  config.vm.provision :shell, path: 'bootstrap.sh', keep_color: true

  config.vm.synced_folder "./src", "/home/ubuntu/projects"

  config.vm.provider 'virtualbox' do |v|
    v.memory = 2048
    v.cpus = 2
  end
end
