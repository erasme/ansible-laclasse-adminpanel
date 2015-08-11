# -*- mode: ruby -*-
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  # config.vm.define "ansible-laclasse-adminpanel" do |nginx|
  # end

  config.vm.provider "virtualbox" do |v|
    v.name   = "ansible-laclasse-adminpanel"
    v.memory = 1024
  end

  config.vm.provision "shell",
    :path => "tests/specs.sh",
    :upload_path => "/home/vagrant/specs",
    # change role name below
    :args => "--install ansible-laclasse-adminpanel"
end
