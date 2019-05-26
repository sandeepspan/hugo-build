+++
date = "2019-05-01T10:54:24+02:00"
title = "Chapter 01"
slug = "openshift-origin-on-vagrant-chapter01"
tags = ["tutorials","openshift","vagrant","virtualbox"]
comments = true # set false to hide Disqus
share = true    # set false to hide share buttons
+++

Welcome, 

Have a great experience with openshift origin on vagrant and virtualbox Chapter 01.

### Prerequisits

Lets have a look on the pre-requisits.

#### Openshift Binaries

* Installable for Windows downloaded from (Link)[https://www.okd.io/download.html]

```
     $ oc version
     oc v1.3.0
     kubernetes v1.3.0+52492b4
     features: Basic-Auth
```

#### VirtualBox

* Installable for Windows downloaded from (Link)[https://www.virtualbox.org/wiki/Downloads] 

#### Vagrant

* Installable for Windows downloaded from (Link)[https://www.vagrantup.com/downloads.htmlhttps://www.vagrantup.com/downloads.html] 
* Vagrantfile can be referred on (Link)[https://app.vagrantup.com/openshift/boxes/origin-all-in-one]
* below is the improvised Vagrantfile content,

```
     Vagrant.configure("2") do |config|
       config.vm.box = "openshift/origin-all-in-one"
     end
```

#### Starting your Vagrant VM

```
# mkdir openshift-allinone

# cd openshift-allinone

# vi Vagrantfile

# cat Vagrantfile
Vagrant.configure("2") do |config|
  config.vm.box = "openshift/origin-all-in-one"
end
# vagrant up
Bringing machine 'default' up with 'virtualbox' provider...
==> default: Box 'openshift/origin-all-in-one' could not be found. Attempting to find and install...
    default: Box Provider: virtualbox
    default: Box Version: >= 0
==> default: Loading metadata for box 'openshift/origin-all-in-one'
    default: URL: https://vagrantcloud.com/openshift/origin-all-in-one
==> default: Adding box 'openshift/origin-all-in-one' (v1.3.0) for provider: virtualbox
    default: Downloading: https://vagrantcloud.com/openshift/boxes/origin-all-in-one/versions/1.3.0/providers/virtualbox.box
    default: Download redirected to host: vagrantcloud-files-production.s3.amazonaws.com
    default:
==> default: Successfully added box 'openshift/origin-all-in-one' (v1.3.0) for 'virtualbox'!
==> default: Importing base box 'openshift/origin-all-in-one'...
==> default: Matching MAC address for NAT networking...
==> default: Checking if box 'openshift/origin-all-in-one' version '1.3.0' is up to date...
==> default: Setting the name of the VM: openshift-origin
==> default: Vagrant has detected a configuration issue which exposes a
==> default: vulnerability with the installed version of VirtualBox. The
==> default: current guest is configured to use an E1000 NIC type for a
==> default: network adapter which is vulnerable in this version of VirtualBox.
==> default: Ensure the guest is trusted to use this configuration or update
==> default: the NIC type using one of the methods below:
==> default:
==> default:   https://www.vagrantup.com/docs/virtualbox/configuration.html#default-nic-type
==> default:   https://www.vagrantup.com/docs/virtualbox/networking.html#virtualbox-nic-type
==> default: Clearing any previously set network interfaces...
==> default: Preparing network interfaces based on configuration...
    default: Adapter 1: nat
    default: Adapter 2: hostonly
==> default: Forwarding ports...
    default: 8443 (guest) => 8443 (host) (adapter 1)
    default: 22 (guest) => 2222 (host) (adapter 1)
==> default: Running 'pre-boot' VM customizations...
==> default: Booting VM...
==> default: Waiting for machine to boot. This may take a few minutes...
    default: SSH address: 127.0.0.1:2222
    default: SSH username: vagrant
    default: SSH auth method: private key
    default: Warning: Connection reset. Retrying...
    default: Warning: Connection aborted. Retrying...
    default: Warning: Remote connection disconnect. Retrying...
    default:
    default: Vagrant insecure key detected. Vagrant will automatically replace
    default: this with a newly generated keypair for better security.
    default:
    default: Inserting generated public key within guest...
    default: Removing insecure key from the guest if it's present...
    default: Key inserted! Disconnecting and reconnecting using new SSH key...
==> default: Machine booted and ready!
==> default: Checking for guest additions in VM...
    default: No guest additions were detected on the base box for this VM! Guest
    default: additions are required for forwarded ports, shared folders, host only
    default: networking, and more. If SSH fails on this machine, please install
    default: the guest additions and repackage the box to continue.
    default:
    default: This is not an error message; everything may continue to work properly,
    default: in which case you may ignore this message.
==> default: Configuring and enabling network interfaces...
==> default: Running provisioner: shell...
    default: Running: inline script
    default: Successfully started and provisioned VM with 2 cores and 5 G of memory.
    default: To modify the number of cores and/or available memory modify your local Vagrantfile
    default:
    default: You can now access the OpenShift console on: https://10.2.2.2:8443/console
    default:
    default: Configured users are (<username>/<password>):
    default: admin/admin
    default: user/user
    default: But, you can also use any username and password combination you would like to create
    default: a new user.
    default: You can find links to the client libraries here: https://www.openshift.org/vm
    default: If you have the oc client library on your host, you can also login from your host.
    default:
    default: To use OpenShift CLI, run:
    default: $ oc login https://10.2.2.2:8443
```

This concludes this chapter, Plese continue reading on next chapter

---

[Contact Us](/)
