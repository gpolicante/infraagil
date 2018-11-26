Vagrant.configure("2") do |config|


   config.vm.define "automation" do |manager|
    manager.vm.box = "centos/7"
        manager.vm.network "private_network", ip: "192.168.33.150"
	manager.vm.hostname = "automation.dexter.com.br" 
       config.vm.provider "virtualbox" do |vb|
        vb.memory = "2048"
        end

   manager.vm.provision "shell", inline: <<-SHELL
	echo "192.168.33.150 automation.dexter.com.br "  >>  /etc/hosts 
	echo "192.168.33.151 devops.dexter.com.br "  >>  /etc/hosts 
	echo "192.168.33.152 docker.dexter.com.br "  >>  /etc/hosts 
	SHELL


        end



   config.vm.define "devops" do |worker1|
    worker1.vm.box = "ubuntu/xenial64"
        worker1.vm.network "private_network", ip: "192.168.33.151"
	worker1.vm.hostname = "devops.dexter.com.br" 

       config.vm.provider "virtualbox" do |vb|
        vb.memory = "1024"
        end

 
   worker1.vm.provision "shell", inline: <<-SHELL
	echo "192.168.33.150 automation.dexter.com.br "  >>  /etc/hosts 
	echo "192.168.33.151 devops.dexter.com.br "  >>  /etc/hosts 
	echo "192.168.33.152 docker.dexter.com.br "  >>  /etc/hosts 
	SHELL

  end


   config.vm.define "docker" do |worker2|
    worker2.vm.box = "ubuntu/xenial64"
        worker2.vm.network "private_network", ip: "192.168.33.152"
	worker2.vm.hostname = "docker.dexter.com.br" 

       config.vm.provider "virtualbox" do |vb|
        vb.memory = "1024"
        end

   worker2.vm.provision "shell", inline: <<-SHELL
	echo "192.168.33.150 automation.dexter.com.br "  >>  /etc/hosts 
	echo "192.168.33.151 devops.dexter.com.br "  >>  /etc/hosts 
	echo "192.168.33.152 docker.dexter.com.br "  >>  /etc/hosts 
	SHELL



end

end












