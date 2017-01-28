# A dummy plugin for Barge to set hostname and network correctly at the very first `vagrant up`
module VagrantPlugins
  module GuestLinux
    class Plugin < Vagrant.plugin("2")
      guest_capability("linux", "change_host_name") { Cap::ChangeHostName }
      guest_capability("linux", "configure_networks") { Cap::ConfigureNetworks }
    end
  end
end

Vagrant.configure(2) do |config|
  config.vm.define "whalebrew-barge"

  config.vm.box = "ailispaw/barge"

  config.vm.synced_folder ".", "/vagrant", id: "vagrant"

  config.vm.provision :shell do |sh|
    sh.privileged = false
    sh.inline = <<-EOT
      sudo /etc/init.d/docker restart v1.13.0

      sudo wget -qO /opt/bin/whalebrew "https://github.com/bfirsh/whalebrew/releases/download/0.0.2/whalebrew-$(uname -s)-$(uname -m)"
      sudo chmod +x /opt/bin/whalebrew

      echo "\nexport WHALEBREW_INSTALL_PATH=/opt/bin" >> ~/.bashrc
    EOT
  end
end
