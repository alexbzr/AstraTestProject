# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # запустить добавленный в вагрант бокс ubuntu 20.04
  config.vm.box = "generic/ubuntu2004"
  config.vm.provider "virtualbox" do |vb|
    vb.name = "ubuntu-ansible"
    # не проверять наличие дополнений гостевой ОС, чтобы не было ошибок
	vb.check_guest_additions = false
    vb.memory = "1536"
    vb.cpus = "2"
  end
  # задать IP адрес машины и пробросить порт 3000 на хост для будущей графаны
  config.vm.network "private_network", ip: "192.168.56.10"
  config.vm.network "forwarded_port", guest: 3000, host: 3000
  
  # загрузить необходимые файлы в vagrant vm для докера
  config.vm.synced_folder "prometheus", "/tmp/prometheus"
  config.vm.synced_folder "grafana", "/tmp/grafana"
  
  # использовать ansible для дальнейшей настройки из файла playbook.yaml
  config.vm.provision "ansible" do |ans|
    ans.playbook = "playbook.yaml"
  end
  
end