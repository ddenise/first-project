Vagrant.configure(2) do |config|
config.vm.provider "virtualbox" do |vb|
  vb.memory = "512"
  vb.cpus = 2
  vb.name = "Vagrant-virtual-machine"
end
config.vm.hostname = "denisa"
config.vm.box = "ubuntu/trusty64"
config.vm.provision "shell", inline: <<-SHELL
  sudo apt-get update
  sudo apt-get install -y git python-pip python-dev
  sudo apt-get -y autoremove
  cd /vagrant
  sudo pip install -r requirements.txt
SHELL
end
