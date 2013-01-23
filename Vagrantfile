# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant::Config.run do |config|
  config.vm.customize ["modifyvm", :id, "--name", "app", "--memory", "512"]
  config.vm.box = "base_lucid64_with_ruby193"
  config.vm.host_name = "app"
  config.vm.forward_port 80, 8000, :auto => true
  config.vm.forward_port 3000, 3000
  config.vm.network :hostonly, "33.33.13.37"
  config.vm.share_folder "puppet", "/etc/puppet", "puppet"
  config.vm.share_folder "app", "/var/www", "app"

  #config.vm.provision :puppet do |puppet|
  #  puppet.manifests_path = "puppet/manifests"
  #  puppet.module_path    = "puppet/modules"
  #  puppet.manifest_file  = "development.pp"
end
