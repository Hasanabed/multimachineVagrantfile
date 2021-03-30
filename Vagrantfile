Vagrant.configure("2") do |config|
  config.vm.define "cenx1" do |cenx1|
    cenx1.vm.box = "centos/7"
    cenx1.vm.hostname = 'CENX1'
    cenx1.vm.box_url = "centos/7"

    cenx1.vm.network :private_network, ip: "192.168.56.101"
    cenx1.vm.network :public_network, bridge: "enp1s0", ip: "192.168.8.31"
    cenx1.vm.network :forwarded_port, guest: 22, host: 10122, id: "ssh"


    cenx1.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 512]
      v.customize ["modifyvm", :id, "--name", "CENX1"]
    end
  end

  config.vm.define "cenx2" do |cenx2|
    cenx2.vm.box = "centos/7"
    cenx2.vm.hostname = 'CENX2'
    cenx2.vm.box_url = "centos/7"

    cenx2.vm.network :private_network, ip: "192.168.56.102"
    cenx2.vm.network :public_network,bridge: "enp1s0", ip: "192.168.8.32"
    cenx2.vm.network :forwarded_port, guest: 22, host: 10222, id: "ssh"

    cenx2.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 256]
      v.customize ["modifyvm", :id, "--name", "CENX2"]
    end
  end

    config.vm.define "cenx3" do |cenx3|
    cenx3.vm.box = "centos/7"
    cenx3.vm.hostname = 'CENX3'
    cenx3.vm.box_url = "centos/7"

    cenx3.vm.network :private_network, ip: "192.168.56.103"
    cenx3.vm.network :public_network, bridge: "enp1s0",ip: "192.168.8.33"
    cenx3.vm.network :forwarded_port, guest: 22, host: 10322, id: "ssh"

    cenx3.vm.provider :virtualbox do |v|
      v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
      v.customize ["modifyvm", :id, "--memory", 512]
      v.customize ["modifyvm", :id, "--name", "CENX3"]
    end
  end

end
