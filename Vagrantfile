Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.box_check_update = false

  config.vm.provision "shell" do |s|
    s.inline = "apt-get update && apt-get install python -yy"
  end

  config.vm.provision :ansible do |ansible|
    ansible.playbook      = "ansible/playbook.yml"
    ansible.sudo          = true
  end


end
