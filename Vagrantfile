Vagrant.configure(2) do |config|
  config.vm.box = "vmware/photon"

  ["vmware_fusion", "vmware_workstation"].each do |p|
    config.vm.provider p do |v|
      v.vmx["memsize"] = "2048"
      v.vmx["numvcpus"] = "2"
      v.vmx["cpuid.coresPerSocket"] = "1"
    end
  end

  config.vm.network "forwarded_port", guest: 80, host: 80
end
