Vagrant.configure(2) do |config|
  config.vm.box = "vmware/photon"

  config.vm.provider "vmware_desktop" do |v|
    v.vmx["memsize"] = "2048"
    v.vmx["numvcpus"] = "2"
    v.vmx["cpuid.coresPerSocket"] = "1"
  end

  config.vm.network "forwarded_port", guest: 80, host: 80
end
