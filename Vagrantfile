# beep
Vagrant.configure("2") do |c|
  c.ssh.forward_agent = true
  c.vm.provider :virtualbox do |v|
    v.customize ["guestproperty", "set", :id, "/VirtualBox/GuestAdd/VBoxService/--timesync-set-threshold", 10000]
  end
  c.vm.box = "drud/applicantbox"
  c.vm.network(:forwarded_port, {:guest=>80, :host=>1025})
  c.vm.synced_folder ".", "/var/www", :mount_options => ["dmode=777", "fmode=666"]
  c.vm.provider :virtualbox do |p|
  end
  c.vm.provision "shell", path: "init", keep_color: false
end
