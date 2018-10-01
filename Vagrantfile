Vagrant.configure("2") do |config|


   config.vm.define "automation" do |manager|
    manager.vm.box = "centos/7"
        manager.vm.network "private_network", ip: "192.168.33.150"
       config.vm.provider "virtualbox" do |vb|
        vb.memory = "2048"
        end

        end



   config.vm.define "devops" do |worker1|
    worker1.vm.box = "ubuntu/xenial64"
        worker1.vm.network "private_network", ip: "192.168.33.151"

       config.vm.provider "virtualbox" do |vb|
        vb.memory = "1024"
        end

   end


   config.vm.define "docker" do |worker2|
    worker2.vm.box = "ubuntu/xenial64"
        worker2.vm.network "private_network", ip: "192.168.33.152"

       config.vm.provider "virtualbox" do |vb|
        vb.memory = "1024"
        end

   end





end

