VAGRANT_VERSION = 2

Vagrant.configure(VAGRANT_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"

  # Make sure to install the vagrant-dns plugin and install resolver
  # https://github.com/BerlinVagrant/vagrant-dns
  config.dns.tld = "dev"
  config.dns.patterns = [/^.*vagrant.dev$/]
  config.vm.hostname = "docker"
  config.vm.network "private_network", ip: "192.168.2.200"

  # Add default ssh public key for remote provisioning
  config.vm.provision "shell" do |shell|
    ssh_public_key = File.read(File.join(Dir.home, ".ssh", "id_rsa.pub"))
    shell.inline = <<-SHELL
      echo 'Copying local ssh public key for remote provisioning'
      mkdir -p /home/vagrant/.ssh
      echo "#{ssh_public_key}" >> /home/vagrant/.ssh/authorized_keys
      echo "#{ssh_public_key}" >> /root/.ssh/authorized_keys
    SHELL
  end

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "playbook.yml"
    ansible.verbose = "v"
  end
end

