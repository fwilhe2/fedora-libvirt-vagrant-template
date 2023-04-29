$script = <<-SCRIPT
sudo dnf -y upgrade

sudo dnf -y install git htop
SCRIPT

Vagrant.configure("2") do |config|
    config.vm.box = "fedora/38-cloud-base"
    config.vm.provider 'libvirt' do |provider|
        provider.memory = 2048
        provider.cpus = 4
    end
    config.vm.provision "shell", inline: $script
end