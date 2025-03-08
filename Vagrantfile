Vagrant.configure("2") do |config|
  # Используем образ Ubuntu 20.04 (или ваш образ, если он специфичен)
  config.vm.box = "spox/ubuntu-arm"
  config.vm.box_version = "1.0.0"

  # Конфигурация для VMware (если это необходимо)
  config.vm.provider :vmware_desktop do |vmware|
    vmware.gui = true
    vmware.cpus = 2
    vmware.vmx["ethernet0.virtualdev"] = "vmxnet3"
    vmware.ssh_info_public = true
    vmware.linked_clone = false
  end

  # Провижионинг с использованием Ansible
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
    ansible.compatibility_mode = "2.0"
    ansible.verbose = "vv"
  end

  # Проброс порта для доступа к Grafana
  config.vm.network "forwarded_port", guest: 3000, host: 3000

  # Проброс порта для Prometheus
  config.vm.network "forwarded_port", guest: 9090, host: 9090

  # Сетевой режим для получения IP в локальной сети
  config.vm.network "public_network"
end