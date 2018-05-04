# TROUBLESHOOTING.md

## On `vagrant up` get VERR_ALREADY_EXISTS error 

### Resolution

* Close the VirtualBox GUI
* after examining the contents of the script run:

```shell
./destroy.sh
```

* run `vagrant up` again

### Error message details

On `vagrant up` you get something like the following message:

```shell
A customization command failed:

["createhd", "--filename", "./zfsDisk_08.vdi", "--variant", "Fixed", "--size", 10240]

The following error was experienced:

#<Vagrant::Errors::VBoxManageError: There was an error while executing `VBoxManage`, a CLI used by Vagrant
for controlling VirtualBox. The command and stderr is shown below.

Command: ["createhd", "--filename", "./zfsDisk_08.vdi", "--variant", "Fixed", "--size", "10240"]

Stderr: 0%...
Progress state: VBOX_E_FILE_ERROR
VBoxManage: error: Failed to create medium
VBoxManage: error: Could not create the medium storage unit '/home/users/someuser/projects/zfs/ansible-role-zfs/zfsDisk_08.vdi'.
VBoxManage: error: VDI: cannot create image '/home/users/someuser/projects/zfs/ansible-role-zfs/zfsDisk_08.vdi' (VERR_ALREADY_EXISTS)
VBoxManage: error: Details: code VBOX_E_FILE_ERROR (0x80bb0004), component MediumWrap, interface IMedium
VBoxManage: error: Context: "RTEXITCODE handleCreateMedium(HandlerArg*)" at line 450 of file VBoxManageDisk.cpp
>

Please fix this customization and try again.
```
