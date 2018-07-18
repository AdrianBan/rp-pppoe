# rp-pppoe - Kernel Mode compilation fix
------------------------------------

This version of RP-PPPoE is the original Debian version 3.12-1.1
with some patches to fix the incorrect detection of Kernel Mode 
of the **./configure** and remove addtional headers which duplicates
the declared constants.

Changelog:

  * Add PPPoE Kernel mode.
  * Patch to remove netinet/in.h and linux/in.h from the tests
    because the if_pppox.h is already including in.h and in6.h
  * Fix configure to detect the kernel mode. 
    #include <netinet/in.h> is duplicating declared constants.
  * Removed the pppoe-server scripts. There is a separate packages
    named pppoe-server which provides systemd bootup services.

