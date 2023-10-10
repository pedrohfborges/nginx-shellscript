Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-22.04"
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.synced_folder "./configs", "/configs"
  config.vm.provision "shell", inline: "hostnamectl hostname NGINX-SERVER && \ sh /configs/script.sh"
  config.vm.network "public_network", ip: "192.168.15.100"
end