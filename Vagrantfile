Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/focal64"
  config.vm.provider "virtualbox" do |virtualbox|
    virtualbox.memory = 512
    virtualbox.cpus = 1
  end

  config.vm.define "docker0" do |docker0|
    docker0.vm.provider "virtualbox" do |virtualbox|
      virtualbox.name = "docker0"
    end
    docker0.vm.network "private_network", ip: "192.168.20.10"
    #Install Docker
    docker0.vm.provision "shell", inline: "curl -fsSL https://get.docker.com -o get-docker.sh && sh get-docker.sh && apt install -y docker-compose-plugin"
    #Set ssh keys
    docker0.vm.provision "shell", inline: "cat /vagrant/configs/ssl/id_bionic.pub >> .ssh/authorized_keys"
  end
  config.vm.define "docker1" do |docker1|
    docker1.vm.provider "virtualbox" do |virtualbox|
      virtualbox.name = "docker1"
    end
    docker1.vm.network "private_network", ip: "192.168.20.20"
    #Install Docker
    docker1.vm.provision "shell", inline: "curl -fsSL https://get.docker.com -o get-docker.sh && sh get-docker.sh && apt install -y docker-compose-plugin"
    #Set ssh keys
    docker1.vm.provision "shell", inline: "cat /vagrant/configs/ssl/id_bionic.pub >> .ssh/authorized_keys"
  end
  config.vm.define "docker2" do |docker2|
    docker2.vm.provider "virtualbox" do |virtualbox|
      virtualbox.name = "docker2"
    end
    docker2.vm.network "private_network", ip: "192.168.20.30"
    #Install Docker
    docker2.vm.provision "shell", inline: "curl -fsSL https://get.docker.com -o get-docker.sh && sh get-docker.sh && apt install -y docker-compose-plugin"
    #Set ssh keys
    docker2.vm.provision "shell", inline: "cat /vagrant/configs/ssl/id_bionic.pub >> .ssh/authorized_keys"
  end
  config.vm.define "docker3" do |docker3|
    docker3.vm.provider "virtualbox" do |virtualbox|
      virtualbox.name = "docker3"
    end
    docker3.vm.network "private_network", ip: "192.168.20.40"
    #Install Docker
    docker3.vm.provision "shell", inline: "curl -fsSL https://get.docker.com -o get-docker.sh && sh get-docker.sh && apt install -y docker-compose-plugin"
    #Set ssh keys
    docker3.vm.provision "shell", inline: "cat /vagrant/configs/ssl/id_bionic.pub >> .ssh/authorized_keys"
  end  
  config.vm.define "docker4" do |docker4|
    docker4.vm.provider "virtualbox" do |virtualbox|
      virtualbox.name = "docker4"
    end
    docker4.vm.network "private_network", ip: "192.168.20.50"
    #Install Docker
    docker4.vm.provision "shell", inline: "curl -fsSL https://get.docker.com -o get-docker.sh && sh get-docker.sh && apt install -y docker-compose-plugin"
    #Set ssh keys
    docker4.vm.provision "shell", inline: "cat /vagrant/configs/ssl/id_bionic.pub >> .ssh/authorized_keys"
  end  
end