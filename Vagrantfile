# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.define "jenkins" do |jenkins|
    jenkins.vm.box = "centos/7"
    jenkins.vm.hostname = 'jenkins'
    jenkins.vm.network :private_network, ip: "192.168.33.10"
    jenkins.vm.provision "ansible" do |ansible|
      ansible.playbook = "setup_jenkins.yml"
    end
  end
end
