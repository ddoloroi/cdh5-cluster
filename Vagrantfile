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

    config.vm.define "hdfs0" do |hdfs0|
	hdfs0.vm.box = box
	hdfs0.vm.host_name = 'hdfs0'
	hdfs0.vm.network :private_network, ip: '172.28.128.34'
	hdfs0.vm.network :forwarded_port, guest: 18081, host:18081
	
	hdfs0.vm.provider "virtualbox" do |v|
	    v.memory = 4096
	    v.cpus = 2
	end

	hdfs0.vm.provision "ansible" do |ansible|
	    ansible.playbook = "playbook.yml"
	end
    end

    config.vm.define "hdfs1" do |hdfs1|
        hdfs1.vm.box = box
        hdfs1.vm.host_name = 'hdfs1'
        hdfs1.vm.network :private_network, ip: '172.28.128.35'
	hdfs1.vm.network :forwarded_port, guest: 18081, host:18082

        hdfs1.vm.provider "virtualbox" do |v|
            v.memory = 4096
	    v.cpus = 2
        end

        hdfs1.vm.provision "ansible" do |ansible|
            ansible.playbook = "playbook.yml"
        end
    end

    config.vm.define "hdfs2" do |hdfs2|
        hdfs2.vm.box = box
        hdfs2.vm.host_name = 'hdfs2'
        hdfs2.vm.network :private_network, ip: '172.28.128.36'
	hdfs2.vm.network :forwarded_port, guest: 18081, host:18083

        hdfs2.vm.provider "virtualbox" do |v|
            v.memory = 4096
	    v.cpus = 2
        end

        hdfs2.vm.provision "ansible" do |ansible|
            ansible.playbook = "playbook.yml"
        end
    end

    config.vm.define "hbase0" do |hbase0|
        hbase0.vm.box = box
        hbase0.vm.host_name = 'hbase0'
        hbase0.vm.network :private_network, ip: '172.28.128.37'

        hbase0.vm.provider "virtualbox" do |v|
            v.memory = 1024
        end

        hbase0.vm.provision "ansible" do |ansible|
            ansible.playbook = "playbook.yml"
        end
    end

    config.vm.define "flume0" do |flume0|
        flume0.vm.box = box
        flume0.vm.host_name = 'flume0'
        flume0.vm.network :private_network, ip: '172.28.128.38'
	flume0.vm.network :forwarded_port, guest: 41414, host:41414
	flume0.vm.network :forwarded_port, guest: 8080, host:8080

        flume0.vm.provider "virtualbox" do |v|
            v.memory = 1024
        end

        flume0.vm.provision "ansible" do |ansible|
            ansible.playbook = "playbook.yml"
        end
    end

    config.vm.define "yarn0" do |yarn0|
        yarn0.vm.box = box
        yarn0.vm.host_name = 'yarn0'
        yarn0.vm.network :private_network, ip: '172.28.128.39'
	yarn0.vm.network :forwarded_port, guest: 8088, host:8088

        yarn0.vm.provider "virtualbox" do |v|
            v.memory = 2048
        end

        yarn0.vm.provision "ansible" do |ansible|
            ansible.playbook = "playbook.yml"
        end
    end

    config.vm.define "hive0" do |hive0|
        hive0.vm.box = box
        hive0.vm.host_name = 'hive0'
        hive0.vm.network :private_network, ip: '172.28.128.40'
	hive0.vm.network :forwarded_port, guest: 8888, host:8888

        hive0.vm.provider "virtualbox" do |v|
            v.memory = 2048
        end

        hive0.vm.provision "ansible" do |ansible|
            ansible.playbook = "playbook.yml"
        end
    end

    config.vm.define "solr0" do |solr0|
        solr0.vm.box = box
        solr0.vm.host_name = 'solr0'
        solr0.vm.network :private_network, ip: '172.28.128.41'

        solr0.vm.provider "virtualbox" do |v|
            v.memory = 1024
        end

        solr0.vm.provision "ansible" do |ansible|
            ansible.playbook = "playbook.yml"
        end
    end

    config.vm.define "spark0" do |spark0|
        spark0.vm.box = box
        spark0.vm.host_name = 'spark0'
        spark0.vm.network :private_network, ip: '172.28.128.42'
	spark0.vm.network :forwarded_port, guest: 18080, host:18080

        spark0.vm.provider "virtualbox" do |v|
            v.memory = 1024
        end

        spark0.vm.provision "ansible" do |ansible|
            ansible.playbook = "playbook.yml"
        end
    end



end
