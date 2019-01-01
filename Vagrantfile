Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"

  config.vm.network "forwarded_port", guest: 3478, host: 3478, protocol: "udp"
  config.vm.network "forwarded_port", guest: 8080, host: 8080, protocol: "tcp"
  config.vm.network "forwarded_port", guest: 8443, host: 8443, protocol: "tcp"
  config.vm.network "forwarded_port", guest: 8880, host: 8880, protocol: "tcp"
  config.vm.network "forwarded_port", guest: 8843, host: 8843, protocol: "tcp"
  config.vm.network "forwarded_port", guest: 6789, host: 6789, protocol: "tcp"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provision.yml"
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "install.yml"
  end
end
