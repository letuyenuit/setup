Vagrant.configure("2") do |config|
  config.vm.define "master" do |master|
    master.vm.box = "ubuntu/focal64"
    master.vm.hostname = "master"
    master.vm.network "private_network", ip: "192.168.56.70"
    master.vm.provider "virtualbox" do |vb|
        vb.memory = 4096
        vb.cpus = 2
    end
  end

  config.vm.define "node1" do |node1|
    node1.vm.box = "ubuntu/focal64"
    node1.vm.hostname = "node1"
    node1.vm.network "private_network", ip: "192.168.56.80"
    node1.vm.provider "virtualbox" do |vb|
        vb.memory = 4096
        vb.cpus = 1
    end
  end

  config.vm.define "jenkins" do |jenkins|
    jenkins.vm.box = "ubuntu/focal64"
    jenkins.vm.hostname = "jenkins"
    jenkins.vm.network "private_network", ip: "192.168.56.90"
    jenkins.vm.provider "virtualbox" do |vb|
        vb.memory = 8092
        vb.cpus = 1
    end
    jenkins.vm.provision "shell", path: "jenkins.sh"
  end
  config.vm.define "agent" do |agent|
    agent.vm.box = "ubuntu/focal64"
    agent.vm.hostname = "agent"
    agent.vm.network "private_network", ip: "192.168.56.95"
    agent.vm.provider "virtualbox" do |vb|
        vb.memory = 2048
        vb.cpus = 1
    end
  end

  config.vm.define "ansible" do |ansible|
    ansible.vm.box = "ubuntu/focal64"
    ansible.vm.hostname = "ansible"
    ansible.vm.network "private_network", ip: "10.10.10.10"
    ansible.vm.provider "virtualbox" do |vb|
        vb.memory = 2048
        vb.cpus = 1
    end
    ansible.vm.disk :disk, name: "backup", size: "1GB"
    ansible.vm.disk :disk, name: "lvm", size: "1GB"
    ansible.vm.disk :disk, name: "extend", size: "1GB"
  end
  config.vm.define "webserver" do |webserver|
    webserver.vm.box = "ubuntu/focal64"
    webserver.vm.hostname = "webserver"
    webserver.vm.network "private_network", ip: "10.10.10.11"
    webserver.vm.provider "virtualbox" do |vb|
        vb.memory = 1024
        vb.cpus = 1
    end
  end
  config.vm.define "dbserver" do |dbserver|
    dbserver.vm.box = "ubuntu/focal64"
    dbserver.vm.hostname = "dbserver"
    dbserver.vm.network "private_network", ip: "10.10.10.12"
    dbserver.vm.provider "virtualbox" do |vb|
        vb.memory = 1024
        vb.cpus = 1
    end
  end
end

