Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
#  config.vm.network "forwarded_port", guest: 8081, host: 8081

  config.vm.provider :virtualbox do |v|
    v.memory = 2048 
  end

  #
  # Run Ansible from the Vagrant Host
  #
  config.vm.provision "ansible_local" do |ansible|
    ansible.install_mode = "pip"
    ansible.version="2.2.2.0"
    ansible.galaxy_role_file = 'requirements.yml'
    ansible.playbook = "playbook.yml"
  end
end

