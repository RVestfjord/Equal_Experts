Content
=======

This repo contains all files necessary to configure and start a Jenkins inside a Vagrant host.
If the file plugins.txt is present and contains a list of plugins during the provisioning the jenkins plugins in that file will be installed automatically.
/var/lib/jenkins of the guest will be exposed as jenkins_var on the host.


Requirements
============

You need to install the vbguest plugin. The plugin is required to install and update vb guest additions. To do so run the following command:
 $ vagrant plugin install vagrant-vbguest

