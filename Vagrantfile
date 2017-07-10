Vagrant.configure("2") do |config|
 
config.vm.define "ghost" do |ghost|
    ghost.vm.box = "ubuntu/trusty64"
    ghost.vm.hostname = "ghost"
    ghost.vm.network "forwarded_port", guest: 80, host: 8080
    ghost.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end
  end
    config.vm.provision "shell", path: "provision.sh"
    config.vm.network "public_network"
end