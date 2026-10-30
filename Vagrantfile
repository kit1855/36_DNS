# -*- mode: ruby -*-
# vim: set ft=ruby :
####################################################################################################
#ns01, ns02, client, client2
####################################################################################################
#  config.vm.define "ns01" do |ns01|
#    ns01.vm.network "private_network", ip: "192.168.50.10", virtualbox__intnet: "dns"
#    ns01.vm.hostname = "ns01"
#  end
#
#  config.vm.define "ns02" do |ns02|
#    ns02.vm.network "private_network", ip: "192.168.50.11", virtualbox__intnet: "dns"
#    ns02.vm.hostname = "ns02"
#  end
#
#  config.vm.define "client" do |client|
#    client.vm.network "private_network", ip: "192.168.50.15", virtualbox__intnet: "dns"
#    client.vm.hostname = "client"
####################################################################################################

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
        ###
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
  # 3. client (AlmaLinux 9)
  # ============================================
  config.vm.define "client" do |client|
    client.vm.box = "almalinux/9"
    client.vm.hostname = "client"
    client.vm.provider "virtualbox" do |v|
      v.memory = 2048
      v.cpus = 2
    end

    client.vm.network "private_network", ip: "192.168.50.15", adapter: 2, netmask: "255.255.255.0", virtualbox__intnet: "dns"

    client.vm.provision "shell",
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
