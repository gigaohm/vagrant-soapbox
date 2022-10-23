# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
  end
  config.vm.box = "ubuntu/jammy64"
  config.vm.define "vagrant-soapbox" do |server|
    server.vm.hostname = "vagrant-soapbox"
  end
  config.vm.provision "ansible" do |ansible|
    # ansible.verbose = "vvv"
    ansible.playbook = "rebased-setup.yml"
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "rebased-configure.yml"
  end
end
