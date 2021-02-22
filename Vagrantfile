Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/xenial64"

    config.vm.define "master"

    config.vm.hostname = "master"

    config.vm.network "forwarded_port", guest: 8000, host: 8050

    config.vm.network "private_network", ip: "192.168.20.100"

    config.vm.synced_folder ".", "/vagrant", type: "virtualbox"

    config.vm.provider "virtualbox" do |v|
        v.name = "Ubuntu k3s"
        v.memory = 2048
        v.cpus = 2
    end
end