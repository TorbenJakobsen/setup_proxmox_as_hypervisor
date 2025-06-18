################################
  Set up Proxmox as Hypervisor
################################

https://www.proxmox.com/

Going forward I will shorten 'Proxmox Virtual Environment' to 'PVE' or 'pve'.

You can find more information and offical documentation here:

- Proxmox VE Documentation - https://pve.proxmox.com/pve-docs/index.html
- Proxmox Support Forum    - https://forum.proxmox.com/
- Proxmox Wiki             - https://pve.proxmox.com/wiki/Main_Page

.. note::

  | PVE is licensed per CPU socket.
  | There is a free tier with only community support and without the enterprise grade components.

****************
  Introduction
****************

Documents my *personal* setup.

.. note::

  | This is not intended for a productive environment!
  | Use at your own risk.


Besides the web console there are other ways to manage a 
Proxmox cluster (also with just one Node).

- Ansible
- Proxmox API: https://pve.proxmox.com/wiki/Proxmox_VE_API
