# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "official-precise32"
  config.vm.box_url = "http://cloud-images.ubuntu.com/vagrant/precise/current/precise-server-cloudimg-i386-vagrant-disk1.box"
  config.vm.provider "virtualbox" do |vb|
    vb.customize ["modifyvm", :id, "--ioapic", "on", "--memory", "2048", "--cpus", "2"]
  end
  config.vm.hostname = "neo4j"
  config.vm.network "forwarded_port", guest: 7474, host: 7474
 # config.vm.network "forwarded_port", guest: 35729, host: 35729
#   config.vm.provision :puppet, :options => "--verbose --debug" do |puppet|
#    puppet.manifests_path = "."
#    puppet.manifest_file  = "vagrant/yeoman.pp"
#    puppet.module_path = "vagrant/modules"
#  end  
  config.vm.provision :shell, :path => "setup.sh"




end
