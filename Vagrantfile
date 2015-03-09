Vagrant.configure(2) do |config|
  config.ssh.insert_key = false

  config.vm.box = "ubuntu/trusty64"

  config.vm.network "forwarded_port", guest: 80, host: 8080
  config.vm.network "forwarded_port", guest: 3000, host: 3000
  config.vm.network "forwarded_port", guest: 9292, host: 9292
  config.vm.network "forwarded_port", guest: 10453, host: 10453
  config.vm.network "forwarded_port", guest: 11371, host: 11371
  
  # Uncomment on Linux/OS X for performance improvements
  # config.vm.network :private_network, ip: '192.168.50.50'
  # config.vm.synced_folder '.', '/vagrant', nfs: true

  # config.vm.provider "virtualbox" do |vb|
  #   vb.customize ["modifyvm", :id, "--natdnsproxy1", "off"]
  #   vb.customize ["modifyvm", :id, "--natdnshostresolver1", "off"]
  # end

  config.vm.provider "virtualbox" do |vb|
    vb.cpus = 4
    vb.memory = "2048"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/ruby_setup/playbook.yml"
    ansible.sudo = true
  end 
end
