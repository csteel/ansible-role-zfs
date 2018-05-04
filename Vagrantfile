# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|  
  config.vm.box = "geerlingguy/ubuntu1604"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  config.vm.network "private_network", ip: "192.168.30.200"

  ZFS_DISK_01 = './zfsDisk_01.vdi'
  ZFS_DISK_02 = './zfsDisk_02.vdi'
  ZFS_DISK_03 = './zfsDisk_03.vdi'
  ZFS_DISK_04 = './zfsDisk_04.vdi'
  ZFS_DISK_05 = './zfsDisk_05.vdi'
  ZFS_DISK_06 = './zfsDisk_06.vdi'
  ZFS_DISK_07 = './zfsDisk_07.vdi'
  ZFS_DISK_08 = './zfsDisk_08.vdi'
  ZFS_DISK_09 = './zfsDisk_09.vdi'
  ZFS_DISK_10 = './zfsDisk_10.vdi'
  ZFS_DISK_11 = './zfsDisk_11.vdi'
  ZFS_DISK_12 = './zfsDisk_12.vdi'
  ZFS_DISK_13 = './zfsDisk_13.vdi'
  ZFS_DISK_14 = './zfsDisk_14.vdi'
  ZFS_DISK_15 = './zfsDisk_15.vdi'
  ZFS_DISK_16 = './zfsDisk_16.vdi'
  ZFS_DISK_17 = './zfsDisk_17.vdi'
  ZFS_DISK_18 = './zfsDisk_18.vdi'
  ZFS_DISK_19 = './zfsDisk_19.vdi'
  ZFS_DISK_20 = './zfsDisk_20.vdi'
  ZFS_DISK_21 = './zfsDisk_21.vdi'
  ZFS_DISK_22 = './zfsDisk_22.vdi'


  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"

    # Building disk files if they don't exist
    if not File.exists?(ZFS_DISK_01)
      vb.customize ['createhd', '--filename', ZFS_DISK_01, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_02)
      vb.customize ['createhd', '--filename', ZFS_DISK_02, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_03)
      vb.customize ['createhd', '--filename', ZFS_DISK_03, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_04)
      vb.customize ['createhd', '--filename', ZFS_DISK_04, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_05)
      vb.customize ['createhd', '--filename', ZFS_DISK_05, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_06)
      vb.customize ['createhd', '--filename', ZFS_DISK_06, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_07)
      vb.customize ['createhd', '--filename', ZFS_DISK_07, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_08)
      vb.customize ['createhd', '--filename', ZFS_DISK_08, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_09)
      vb.customize ['createhd', '--filename', ZFS_DISK_09, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_10)
      vb.customize ['createhd', '--filename', ZFS_DISK_10, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_11)
      vb.customize ['createhd', '--filename', ZFS_DISK_11, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_12)
      vb.customize ['createhd', '--filename', ZFS_DISK_12, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_13)
      vb.customize ['createhd', '--filename', ZFS_DISK_13, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_14)
      vb.customize ['createhd', '--filename', ZFS_DISK_14, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_15)
      vb.customize ['createhd', '--filename', ZFS_DISK_15, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_16)
      vb.customize ['createhd', '--filename', ZFS_DISK_16, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_17)
      vb.customize ['createhd', '--filename', ZFS_DISK_17, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_18)
      vb.customize ['createhd', '--filename', ZFS_DISK_18, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_19)
      vb.customize ['createhd', '--filename', ZFS_DISK_19, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_20)
      vb.customize ['createhd', '--filename', ZFS_DISK_20, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_21)
      vb.customize ['createhd', '--filename', ZFS_DISK_21, '--variant', 'Fixed', '--size', 10 * 1024]
    end
    if not File.exists?(ZFS_DISK_22)
      vb.customize ['createhd', '--filename', ZFS_DISK_22, '--variant', 'Fixed', '--size', 10 * 1024]
      # Adding a SATA controller that allows 4 hard drives
      vb.customize ['storagectl', :id, '--name', 'SATA Controller', '--add', 'sata', '--portcount', 30]
      # Attaching the disks using the SATA controller
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 1, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_01]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 2, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_02]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 3, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_03]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 4, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_04]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 5, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_05]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 6, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_06]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 7, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_07]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 8, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_08]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 9, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_09]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 10, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_10]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 11, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_11]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 12, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_12]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 13, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_13]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 14, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_14]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 15, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_15]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 16, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_16]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 17, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_17]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 18, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_18]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 19, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_19]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 20, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_20]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 21, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_21]
      vb.customize ['storageattach', :id,  '--storagectl', 'SATA Controller', '--port', 22, '--device', 0, '--type', 'hdd', '--medium', ZFS_DISK_22]

    end
  end
# zpool create command will do all this
#  config.vm.provision "shell", inline: <<-SHELL
#    sudo mkfs.ext4 /dev/sdb
#    sudo mkfs.ext4 /dev/sdc
#    sudo mkfs.ext4 /dev/sdd
#    sudo mkfs.ext4 /dev/sde
#    sudo mkfs.ext4 /dev/sdf
#    sudo mkfs.ext4 /dev/sdg
#    sudo mkfs.ext4 /dev/sdh
#    sudo mkfs.ext4 /dev/sdi
#  SHELL

  config.vm.provision "ansible" do |ansible|
      ansible.playbook = 'tests/vagrant.yml'
  end
  config.vm.synced_folder ".", "/vagrant", disabled: true
end  
