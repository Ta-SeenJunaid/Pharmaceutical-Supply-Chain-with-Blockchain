$script = <<-SCRIPT

echo "cd /vagrant" >> /home/vagrant/.profile
echo "cd /vagrant" >> /home/vagrant/.bashrc
echo "All good!!"
SCRIPT

Vagrant.configure("2") do |config|

    # Ubuntu 64 bit
    config.vm.box = "bento/ubuntu-16.04"


    config.ssh.username = 'vagrant'
    config.ssh.password = 'vagrant'
    config.ssh.insert_key = 'true'


    # Ports foward
    # For Orderer Container
    config.vm.network "forwarded_port", guest: 7050, host: 7050

    #Explorer
    config.vm.network "forwarded_port", guest: 8080, host: 8080
    #CouchDB
    config.vm.network "forwarded_port", guest: 5984, host: 5984


    # For Peer Container
    config.vm.network "forwarded_port", guest: 7051, host: 7051
    config.vm.network "forwarded_port", guest: 7052, host: 7052
    config.vm.network "forwarded_port", guest: 8051, host: 8051
    config.vm.network "forwarded_port", guest: 8052, host: 8052
    config.vm.network "forwarded_port", guest: 9051, host: 9051
    config.vm.network "forwarded_port", guest: 9052, host: 9052
    config.vm.network "forwarded_port", guest: 10051, host: 10051
    config.vm.network "forwarded_port", guest: 10052, host: 10052
    config.vm.network "forwarded_port", guest: 11051, host: 11051
    config.vm.network "forwarded_port", guest: 11052, host: 11052
    config.vm.network "forwarded_port", guest: 12051, host: 12051
    config.vm.network "forwarded_port", guest: 12052, host: 12052
    config.vm.network "forwarded_port", guest: 13051, host: 13051
    config.vm.network "forwarded_port", guest: 13052, host: 13052
    config.vm.network "forwarded_port", guest: 14051, host: 14051
    config.vm.network "forwarded_port", guest: 14052, host: 14052
    config.vm.network "forwarded_port", guest: 15051, host: 15051
    config.vm.network "forwarded_port", guest: 15052, host: 15052
    config.vm.network "forwarded_port", guest: 16051, host: 16051
    config.vm.network "forwarded_port", guest: 16052, host: 16052
    



    config.vm.provision "shell", inline:  $script

 
    config.vm.provider :virtualbox do |vb|

      vb.customize ["modifyvm", :id, "--memory", "3072", "--cpus", "1"]
      # Change this only if you need desktop for Ubuntu - you will need more memory
      vb.gui = false
      
    end

    # Configuration for Windows Hyperv
    config.vm.provider :hyperv do |hv|
      hv.customize ["modifyvm", :id, "--memory", "3072", "--cpus", "1"]
      # Change this only if you need destop for Ubuntu - you will need more memory
      hv.gui = false

    end


  end