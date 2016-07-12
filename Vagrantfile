# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "bento/ubuntu-16.04"
  config.vm.network "forwarded_port", guest: 80, host: 8000
  config.vm.provision "ansible" do |ansible|
     # ansible.verbose="vvvv"
     # ansible.tags=["content"]
     ansible.playbook = "provisioning/playbook.yml"
     # alternatively run the playbook from the shell like this:
     #    ansible-playbook -i "testserver.com," playbook.yml
  end
end
