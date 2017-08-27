$script = <<SCRIPT
   sudo apt-get update
   sudo apt-get -y install openjdk-8-jdk
   sudo apt-get -y install tomcat8
SCRIPT

Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: $script
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "forwarded_port", guest: 8080, host: 8888
  config.vm.provider "virtualbox" do |v|
    v.name = "trusty-openjdk8-tomcat8"
  end
end
