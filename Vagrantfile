Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  
  config.vm.define "vagrant1" do |vagrant1|
    vagrant1.vm.box = "centos/7"
    vagrant1.vm.network "forwarded_port", guest: 6443, host: 6443
  end
  config.vm.define "vagrant2" do |vagrant2|
    vagrant2.vm.box = "centos/7"
  end

  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 2
  end
end