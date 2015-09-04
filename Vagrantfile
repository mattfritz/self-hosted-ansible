Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  ssh_public_key = File.read(File.join(Dir.home, ".ssh", "id_rsa.pub"))
  ssh_script = "sudo apt-get update && echo #{ssh_public_key} >> /home/vagrant/.ssh/authorized_keys"

  # Make sure to install the vagrant-dns plugin and install resolver
  # https://github.com/BerlinVagrant/vagrant-dns
  config.dns.tld = "dev"
  config.dns.patterns = [/^.*vagrant.dev$/]
  config.vm.hostname = "docker"
  config.vm.network "private_network", ip: "192.168.2.200"

  # Add ssh key from home dir
  config.vm.provision "shell", inline: ssh_script

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "playbook.yml"
    ansible.extra_vars = { ansible_ssh_user: 'vagrant' }
    ansible.verbose = "v"
  end
end

