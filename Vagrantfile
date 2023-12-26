Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu2304"

  config.vm.network :forwarded_port, guest: 22, host: 2323
  config.vm.provider "qemu" do |qe|
    qe.arch = "x86_64"
    qe.machine = "q35"
    qe.cpu = "max"
    qe.net_device = "virtio-net-pci"
    qe.memory = "8G"
    qe.qemu_dir = "/opt/homebrew/share/qemu"
  end

  # config.vm.provider :vmware_desktop do |v|
  #   v.vmx["ethernet0.pcislotnumber"] = "160"
  # end

  # config.vm.provider :vmware_fusion do |v|
  #   v.vmx["ethernet0.pcislotnumber"] = "160"
  # end

  # config.vm.provider "parallels" do |prl|
  #   prl.memory = 1024
  #   prl.cpus = 2
  # end

  # config.vm.provider "docker" do |d|
  #   d.image = "ubuntu"
  #   d.platform = "x86_64"
  # end
end