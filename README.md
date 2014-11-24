vagrant-riak.2.0.2-ubuntu-13.04
===============================

Vagrant files to install Riak 2.0.2 on an Ubuntu Raring Ringtail 13.04

Current Status - Alpha
----------------------

This file is in development and will be subject to change.

Purpose
-------

The is a basic headless server running Riak 2.0.2 as a service with 5 riak instances running on it and all their appropriate ports exposed to the host machine.

Customising
-----------

The 'normal' thing to customise in these files is the location of the directory on the host machine to mount on the guest server - see later for details of how to change that.

How To Use
----------

Install Vagrant on your host machine:
https://www.vagrantup.com/downloads.html

Go to a directory on your host machine:
``vagrant init``

Then copy down the two files from here:
* ``Vagrantfile``
* ``provision-riak-2.0.2-vagrant``

You will need to overwrite the ``Vagrantfile`` that you created when you inited the directory

Then simpyly start the virtual machine with:
``vagrant up``

and take it down with:
``vagrant halt``

You can shell into the machine with SSH on port 2222.

It will mount some local files on your vagrant machine at ``/home/vagrant/vagrant_files``

**YOU MIGHT WANT TO CHANGE THE MOUNT POINT ON YOUR HOST MACHINE** by editing the ``Vagrantfile``

If you install an X-Server on your host you can start GUI apps on the Riak box. For windows use XMing:
http://sourceforge.net/projects/xming/

For the Mac use XQuartz:
http://xquartz.macosforge.org/trac/wiki


