# vpls-openbsd-vnx

This scenario is the VNX implementation of the basic VPLS test setup for OpenBSD, described in the link https://github.com/rwestphal/openbsd-ldpd/wiki/VPLS-basic-test-setup

All nodes shown in the OpenBSD VPLS test setup are implemented here as virtualized OpenBSD machines. 

As indicated in the OpenBSD VPLS test setup, reassembly should be disabled in the Px nodes. You may do this configuring the OpenBSD packet filter with the "set reassemble no" instruction. Alternatively, and this is what is configured in the VNX implementation of the scenario, you may fully disable the packet filter.

Preparation of the scenario:

- Installation of VNX in the virtualization host. Follow the instructions provided in the VNX page: http://web.dit.upm.es/vnxwiki/index.php/Vnx-install  
  If you already had an installation of VNX, update to the last version using the vnx_update command (as root).

- Creation of the OpenBSD root filesystem. Follow the instructions provided in the VNX page: http://web.dit.upm.es/vnxwiki/index.php/Vnx-rootfsopenbsd
- Download the VNX scenario definition file vpls-openbsd.xml.
- Download the folder vpls-conf to the same directory as vpls-openbsd.xml.
- Edit vpls-openbsd.xml and change the name in filesystem tags to match the name of the root filesystem created before.

Starting the scenario:
- Start the VNX scenario with the -t option: vnx -f vpls-openbsd.xml -t
- Logon to the consoles of the CE machines and verify connectivity with pings.

