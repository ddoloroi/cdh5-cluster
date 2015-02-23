VAGRANTFILE_API_VERSION = 2

box = 'chef/centos-6.6'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

    config.vm.define "cdh" do |cdh|
        cdh.vm.box = box
        cdh.vm.host_name = 'cdh'
	cdh.vm.network :private_network, ip: '172.28.128.30'
        cdh.vm.network :forwarded_port, guest: 7180, host:7180

        cdh.vm.provider "virtualbox" do |v|
            v.memory = 6144
	    v.cpus = 2
        end

	cdh.vm.provision "ansible" do |ansible|
            ansible.playbook= "playbook.yml"
        end

    end

    config.vm.define "zookeeper0" do |zk0|
        zk0.vm.box = box
        zk0.vm.host_name = 'zookeeper0'
        zk0.vm.network :private_network, ip: '172.28.128.31'

        zk0.vm.provider "virtualbox" do |v|
            v.memory = 512
        end

	zk0.vm.provision "ansible" do |ansible|
	    ansible.playbook= "playbook.yml"
	end
    end

    config.vm.define "zookeeper1" do |zk1|
        zk1.vm.box = box
        zk1.vm.host_name = 'zookeeper1'
        zk1.vm.network :private_network, ip: '172.28.128.32'

        zk1.vm.provider "virtualbox" do |v|
            v.memory = 512
        end

        zk1.vm.provision "ansible" do |ansible|
            ansible.playbook= "playbook.yml"
        end
    end

    config.vm.define "zookeeper2" do |zk2|
        zk2.vm.box = box
        zk2.vm.host_name = 'zookeeper2'
        zk2.vm.network :private_network, ip: '172.28.128.33'

        zk2.vm.provider "virtualbox" do |v|
            v.memory = 512
        end

        zk2.vm.provision "ansible" do |ansible|
            ansible.playbook= "playbook.yml"
        end
    end

end
