Vagrant.configure("2") do |config|
  #node1
  config.vm.define "node1" do |node1|
    node1.vm.box = "ubuntu"
    node1.vm.network "private_network", ip: "192.168.33.101"
    node1.vm.hostname = "node1"
    node1.vm.provision "shell", inline: <<-SHELL
        apt-get update
        chpasswd <<<"root:node1"
        hostnamectl set-hostname node1
        sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/g' /etc/ssh/sshd_config
        systemctl restart sshd
        apt-get install ca-certificates curl
        install -m 0755 -d /etc/apt/keyrings
        curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
        chmod a+r /etc/apt/keyrings/docker.asc
        echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null
        apt-get update
        apt-get install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
    SHELL
    node1.vm.provider "virtualbox" do |v|
      v.memory = 512
      v.cpus = 1
      v.gui = false
      v.linked_clone = true
    end
  end
  #node2
  config.vm.define "node2" do |node2|
    node2.vm.box = "ubuntu"
    node2.vm.network "private_network", ip: "192.168.33.102"
    node2.vm.hostname = "node2"
    node2.vm.provision "shell", inline: <<-SHELL
        apt-get update
        chpasswd <<<"root:node2"
        hostnamectl set-hostname node2
        sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/g' /etc/ssh/sshd_config
        systemctl restart sshd
        apt-get install ca-certificates curl
        install -m 0755 -d /etc/apt/keyrings
        curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
        chmod a+r /etc/apt/keyrings/docker.asc
        echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null
        apt-get update
        apt-get install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
    SHELL
    node2.vm.provider "virtualbox" do |v|
      v.memory = 512
      v.cpus = 1
      v.gui = false
    end
  end
  #node3
  config.vm.define "node3" do |node3|
    node3.vm.box = "ubuntu"
    node3.vm.network "private_network", ip: "192.168.33.103"
    node3.vm.hostname = "node3"
    node3.vm.provision "shell", inline: <<-SHELL
        apt-get update
        chpasswd <<<"root:node3"
        hostnamectl set-hostname node3
        sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/g' /etc/ssh/sshd_config
        systemctl restart sshd
        apt-get install ca-certificates curl
        install -m 0755 -d /etc/apt/keyrings
        curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
        chmod a+r /etc/apt/keyrings/docker.asc
        echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null
        apt-get update
        apt-get install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
    SHELL
    node3.vm.provider "virtualbox" do |v|
      v.memory = 512
      v.cpus = 1
      v.gui = false
    end
  end
  #node4
  config.vm.define "node4" do |node4|
    node4.vm.box = "ubuntu"
    node4.vm.network "private_network", ip: "192.168.33.104"
    node4.vm.hostname = "node4"
    node4.vm.provision "shell", inline: <<-SHELL
        apt-get update
        chpasswd <<<"root:node4"
        hostnamectl set-hostname node4
        sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/g' /etc/ssh/sshd_config
        systemctl restart sshd
        apt-get install ca-certificates curl
        install -m 0755 -d /etc/apt/keyrings
        curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
        chmod a+r /etc/apt/keyrings/docker.asc
        echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null
        apt-get update
        apt-get install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
    SHELL
    node4.vm.provider "virtualbox" do |v|
      v.memory = 512
      v.cpus = 1
      v.gui = false
    end
  end
end
