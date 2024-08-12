Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/bionic64"
    config.vm.provider "virtualbox" do |vb|
      vb.memory = "256"
      vb.cpus = 1
    end
  
    (1..3).each do |i|
      config.vm.define "server#{i}" do |server|
        server.vm.hostname = "server#{i}"
        server.vm.network "private_network", type: "dhcp"
      end
    end
  end
  