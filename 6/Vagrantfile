Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.hostname = "projectwork10"

  config.vm.provision "shell", privileged: true, inline: <<-SHELL
    sudo apt-get update
    sudo apt-get install -y python3 python3-pip
    sudo apt-get install -y libpq-dev
    sudo pip3 install psycopg2 Django
    sudo mkdir -p /opt/obmen
    sudo cp /vagrant/empty.txt /opt/obmen
  SHELL

  config.vm.synced_folder ".", "/vagrant"
end

