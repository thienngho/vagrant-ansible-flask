VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.define :absolute do |absolute|
    absolute.vm.box = 'ubuntu/xenial64'
    absolute.vm.network "private_network", ip: "192.168.50.2"
  end

  config.vm.provision 'ansible' do |ansible|
    ansible.playbook = 'ansible/dev.yml'
  end

  config.vm.provider "virtualbox" do |v|
    v.memory = 1048
    v.cpus = 1
  end
end
