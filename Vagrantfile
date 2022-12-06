# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
 config.vm.box_check_update = "false"
 config.vm.provider "virtualbox" do |vb|
   vb.memory = "1024"
 end
 #Déclaration d'une VM
 config.vm.define "webserver" do |web|
   web.vm.hostname = "mwiws01" #VM name
   web.vm.box = "debian/buster64"
   web.vm.network :private_network, ip: "192.168.10.10"
   web.vm.network "forwarded_port", guest: "80", host: "8083"
   # Synchronize ?
   #web.vm.synced_folder "/apps/shared", "/shared"

   #Provision the webserver with Ansible

   #web.vm.provision "ansible" do |ansible|
   #  ansible.playbook="apache-playbook.yaml"
   #end

  end


  #Déclaration de la box 2
  #config.vm.define "vm2" do |vm2|
  # vm2.vm.box = "centos/7"
  # vm2.vm.hostname = 'vm2'
  # vm2.vm.box_url = "centos/7"
  # vm2.vm.network "public_network", bridge: "en0: Wi-Fi (AirPort)", auto_config: false
  # vm2.vm.provision "shell", inline: $systemcmd
  #end

end