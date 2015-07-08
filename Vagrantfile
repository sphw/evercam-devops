Vagrant.configure(2) do |config|
  config.ssh.insert_key = false

  config.vm.box = "evercam_box"
  config.vm.box_url = "https://dl.dropboxusercontent.com/s/nyx698gadrote0z/devops.box"

  config.ssh.username = "vagrant"
  config.ssh.password = "vagrant"

  config.vm.network :forwarded_port, guest: 80, host: 8080
  config.vm.network :forwarded_port, guest: 3000, host: 3000
  config.vm.network :forwarded_port, guest: 4000, host: 4000
  config.vm.network :forwarded_port, guest: 9292, host: 9292
  config.vm.network :private_network, ip: '192.168.50.50'

  # Uncomment on Linux/OS X for performance improvements
  #
  # config.vm.synced_folder '.', '/vagrant', nfs: true
  #
  # config.vm.provider "virtualbox" do |vb|
  #   vb.customize ["modifyvm", :id, "--natdnsproxy1", "off"]
  #   vb.customize ["modifyvm", :id, "--natdnshostresolver1", "off"]
  # end

  config.vm.provider "virtualbox" do |vb|
    vb.cpus = 4
    vb.memory = "2048"

    # Uncomment in case of connection problems
    # vb.gui = true
  end
end
