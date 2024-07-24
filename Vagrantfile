Vagrant.configure("2") do |config|
  config.vm.define "master" do |master|
    master.vm.box = "ubuntu/focal64"
    master.vm.hostname = "master"
    master.vm.network "private_network", ip: "192.168.56.70"
    master.vm.provider "virtualbox" do |vb|
        vb.memory = 4096
        vb.cpus = 2
    end
    master.vm.provision "shell", path: "master.sh"
  end

  config.vm.define "node1" do |node1|
    node1.vm.box = "ubuntu/focal64"
    node1.vm.hostname = "node1"
    node1.vm.network "private_network", ip: "192.168.56.80"
    node1.vm.provider "virtualbox" do |vb|
        vb.memory = 4096
        vb.cpus = 1
    end
    node1.vm.provision "shell", path: "common.sh"
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

  # config.vm.define "backstage" do |backstage|
  #   backstage.vm.box = "ubuntu/focal64"
  #   backstage.vm.hostname = "backstage"
  #   backstage.vm.network "private_network", ip: "192.168.56.100"
  #   backstage.vm.provider "virtualbox" do |vb|
  #       vb.memory = 8092
  #       vb.cpus = 1
  #   end
  # end

  # config.vm.define "postgresql" do |postgresql|
  #   postgresql.vm.box = "ubuntu/focal64"
  #   postgresql.vm.hostname = "postgresql"
  #   postgresql.vm.network "private_network", ip: "192.168.56.110"
  #   postgresql.vm.provider "virtualbox" do |vb|
  #       vb.memory = 3072
  #       vb.cpus = 1
  #   end
  # end
end

