################################
  Set up Proxmox as Hypervisor
################################

https://www.proxmox.com/

****************
  Introduction
****************

Documents my *personal* setup.

A better way is to use Ansible, and I will get there eventually.

Initial Housekeeping
====================


Templates
=========

Example for Debian/Ubuntu.

Optionally install QEMU


Optionally install CloudInit

.. code-block: bash

sudo apt install cloud-init

Reset SSH host keys

.. code-block: bash
  cd /etc/ssh
  sudo rm ssh_host_*

Missing will trigger CloudInit to create.

Machine dependencies

The machine id needs to be unique

.. code: bash

  cat /etc/machine-id
    
  sudo truncate -s 0 /etc/machine-id

Also check symbolic link

  /var/lib/dbus/machine-id

Create it if missing

.. code: bash

  sudo ln -s /etc/machine-id /var/lib/dbus/machine-id

Clean out 

.. code: bash

  sudo apt clean
  sudo apt autoremove


Shut down to make cahnges in PVE console

- Convert to Template
- Remove CD ROM iso if present
- add  CloudInit drive
- edit canges in CloudInit drive. eg user
- click regenerate image

| Ready for "clone" Template
| Prefer full clone instead of "linked"


Update hostname

.. code:

  sudo nano /etc/hostname

  sudo nano /etc/hosts
  
