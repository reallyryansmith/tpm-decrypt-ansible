luks-pass-change
=========

This playbook will check that a LUKS encrypted drive you provide with variable 'crypt_device' is present, (encrypted drive should already be open, these tasks are being written to replace the encryption key from one set in a kickstart), the playbook then adds a new password (not stored somewhere in plain text), and then removes the insecure kickstart's set password.  

Requirements
------------
crypsetup packages will be installed

Role Variables
--------------

crypt_device: partition that is encrypted (such as /dev/nvme1n1)
