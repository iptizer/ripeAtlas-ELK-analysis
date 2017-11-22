# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.define "ripeAtlas-ELK-analysis" do |web|
    web.vm.box = "centos/7"
    web.vm.network "forwarded_port",guest:22,host:2200
    web.vm.network "forwarded_port",guest:80,host:8080
    web.vm.network "forwarded_port",guest:443,host:8443
    #web.vm.network "forwarded_port",guest:9090,host:9090
  end
  config.vm.provider "virtualbox" do |vb|
    vb.memory = 8192
    vb.cpus = 4
  end

end
