# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  #Puppet Lab's CentOS Boxes
  #https://github.com/puppetlabs/puppet-vagrant-boxes

  #Vanilla
  #config.vm.box = "centos-64-x64-vbox4210-nocm"
  #config.vm.box_url = "http://puppet-vagrant-boxes.puppetlabs.com/centos-64-x64-vbox4210-nocm.box"

  #Puppet (I already have this on my machine, using to save time)
  config.vm.box = "centos-64-x64-vbox4210"
  config.vm.box_url = "http://puppet-vagrant-boxes.puppetlabs.com/centos-64-x64-vbox4210.box"

  # Port forward 80 to 8080
  config.vm.network :forwarded_port, guest: 80, host: 8080

  #Install lamp and so on
  #In future will probably swap this out with something like Puppet
  config.vm.provision :shell, :path => "environment/bootstrap.sh"

end