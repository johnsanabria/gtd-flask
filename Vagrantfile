Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.synced_folder "/Users/johnsanabria/Src/Asignaciones/DS/WebServices", "/code"
  config.vm.network "forwarded_port", guest: 5000, host: 5000
  config.vm.provider :virtualbox do |vb|
    vb.customize [ 'modifyvm', :id, '--name', 'flask' ]
  end
end
