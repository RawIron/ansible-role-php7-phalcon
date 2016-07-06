
Vagrant.configure(2) do |config|

  config.vm.box = "ansible-role-php7-phalcon_ubuntu-14.04"
  config.vm.box_url = "trusty-server-cloudimg-amd64-vagrant-disk1.box"

  config.vm.network "public_network"

  config.vm.provider "virtualbox" do |vb|
    vb.gui = false
    vb.memory = "2048"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "vagrant_playbook.yml"
    ansible.verbose = "vvvv"
  end

end
