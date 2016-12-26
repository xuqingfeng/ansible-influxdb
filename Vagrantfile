Vagrant.configure("2") do |config|

  config.vm.box = "centos/7"
  config.vm.box_check_update = false
  config.ssh.forward_agent = true
  config.ssh.insert_key = false

  config.vm.provider "virtualbox" do |vb|
    vb.cpus = 1
    vb.memory = 512
  end

  config.vm.define "influxdb-" do | machine |
    machine.vm.hostname = "influxdb"
    machine.vm.network "private_network", ip: "10.0.233.1"

    machine.vm.provision "ansible" do |ansible|
      ansible.sudo = true
      ansible.playbook = "test.yml"
    end
  end

end
