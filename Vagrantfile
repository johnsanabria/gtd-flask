Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.provider :virtualbox do |vb|
    vb.customize [ 'modifyvm', :id, '--name', 'flask' ]
  end
end
