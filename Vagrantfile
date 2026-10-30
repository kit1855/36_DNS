# -*- mode: ruby -*-
# vim: set ft=ruby :

# Указываем зеркало для скачивания образов
ENV['VAGRANT_SERVER_URL'] = 'https://vagrant.elab.pro'

Vagrant.configure("2") do |config|

  # ============================================
  # 1. ns01 (AlmaLinux 9)
  # ============================================
  config.vm.define "ns01" do |ns01|
    ns01.vm.box = "almalinux/9"
    ns01.vm.hostname = "ns01"
    ns01.vm.provider "virtualbox" do |v|
      v.memory = 2048
      v.cpus = 2
    end

    ns01.vm.network "private_network", ip: "192.168.50.10", adapter: 2, netmask: "255.255.255.0", virtualbox__intnet: "dns"

    ns01.vm.provision "shell",
      run: "always",
      inline: <<-SHELL

        # установка пакетов
        sudo dnf install -y bind bind-utils

        # NAMED.DNS.LAB
        sudo cp /vagrant/provisioning/named.dns.lab /etc/named/named.dns.lab
        sudo cp /vagrant/provisioning/master-named.conf /etc/named.conf
        sudo named-checkconf                                                     # проверка конфига
        sudo named-checkzone dns.lab /etc/named/named.dns.lab                    # проверка зоны
        sudo systemctl enable --now named                                        # запуск сервиса

    SHELL
  end

  # ============================================
  # 2. ns02 (AlmaLinux 9)
  # ============================================
  config.vm.define "ns02" do |ns02|
    ns02.vm.box = "almalinux/9"
    ns02.vm.hostname = "ns02"
    ns02.vm.provider "virtualbox" do |v|
      v.memory = 2048
      v.cpus = 2
    end

    ns02.vm.network "private_network", ip: "192.168.50.11", adapter: 2, netmask: "255.255.255.0", virtualbox__intnet: "dns"

    ns02.vm.provision "shell",
      run: "always",
      inline: <<-SHELL
        ###
    SHELL
  end

  # ============================================
  # 3. client1 (AlmaLinux 9)
  # ============================================
  config.vm.define "client1" do |client1|
    client1.vm.box = "almalinux/9"
    client1.vm.hostname = "client1"
    client1.vm.provider "virtualbox" do |v|
      v.memory = 2048
      v.cpus = 2
    end

    client1.vm.network "private_network", ip: "192.168.50.15", adapter: 2, netmask: "255.255.255.0", virtualbox__intnet: "dns"

    client1.vm.provision "shell",
      run: "always",
      inline: <<-SHELL
        ###
    SHELL
  end

  # ============================================
  # 4. client2 (AlmaLinux 9)
  # ============================================
  config.vm.define "client2" do |client2|
    client2.vm.box = "almalinux/9"
    client2.vm.hostname = "client2"
    client2.vm.provider "virtualbox" do |v|
      v.memory = 2048
      v.cpus = 2
    end

    client2.vm.network "private_network", ip: "192.168.50.16", adapter: 2, netmask: "255.255.255.0", virtualbox__intnet: "dns"

    client2.vm.provision "shell",
      run: "always",
      inline: <<-SHELL
        ###
    SHELL
  end

end
