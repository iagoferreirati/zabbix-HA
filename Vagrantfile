Vagrant.configure("2") do |config|
  config.vm.define "node1" do |node1|
    node1.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end      
    node1.vm.box = "centos/8"
    node1.vm.network "public_network", ip: "192.168.1.100", bridge: "wlp3s0"
    node1.vm.provider "virtualbox" do |vb|
      # Customize the amount of memory on the VM:
      vb.memory = "2048"
    end        
  end

  config.vm.define "node2" do |node2|
    node2.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end      
    node2.vm.box = "centos/8"
    node2.vm.network "public_network", ip: "192.168.1.101", bridge: "wlp3s0"
    node2.vm.provider "virtualbox" do |vb|
      # Customize the amount of memory on the VM:
      vb.memory = "2048"
    end
  end
end