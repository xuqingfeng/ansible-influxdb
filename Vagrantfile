Vagrant.configure("2") do |config|

  config.vm.box = "centos/7"
  #config.vm.box = ""
  config.vm.box_check_update = false

  BOX_COUNT = 1
  (1..BOX_COUNT).each do | machine_id |
    config.vm.define "influxdb#{machine_id}" do | machine |
      machine.vm.hostname = "influxdb#{machine_id}"
      machine.vm.network "private_network", ip: "10.0.233.#{1+machine_id}"

      machine.vm.provider "virtualbox" do |v|
        v.memory = 512
        v.cpus = 1
      end

      if machine_id == BOX_COUNT

        machine.vm.provision "ansible" do |ansible|
          ansible.sudo = true
          ansible.playbook = "test.yml"
        end

      end

    end

  end

end
