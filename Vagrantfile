Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  config.vm.network "forwarded_port", guest: 8080, host: 8080

  config.vm.synced_folder "jenkins_var/", "/var/lib/jenkins", create: true
  
  config.vm.provision "shell" do |s|
    s.binary = true
    s.inline = " yum install -y epel-release
                 yum install -y \
			ansible \
			python-pip \
                        python-wheel
                 ansible-playbook /vagrant/playbook.yml"
  end
end
