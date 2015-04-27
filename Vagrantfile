Vagrant.configure(2) do |config|
  config.vm.box = 'precise64'
  config.vm.box_url = 'http://cloud-images.ubuntu.com/vagrant/precise/current/precise-server-cloudimg-amd64-vagrant-disk1.box'
  config.vm.hostname = 'rails-vm'
  config.vm.network :private_network, type: 'dhcp'
  config.vm.provider 'virtualbox' do |vb|
    vb.memory = 1024
  end
  config.vm.provision :ansible do |a|
    a.playbook = 'provisioning/playbook.yml'
  end
end
