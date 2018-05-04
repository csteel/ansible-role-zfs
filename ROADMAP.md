# ROADMAP.md

## Notes

### Depreciated usage of ansible zfs module

```shell
TASK [../../ : manage_zfs | managing pools] ************************************
changed: [default] => (item={u'compression': u'lz4', u'devices': [u'raidz2 /dev/sdb /dev/sdc /dev/sdd /dev/sde /dev/sdf /dev/sdg /dev/sdh', u'raidz2 /dev/sdi /dev/sdj /dev/sdk /dev/sdl /dev/sdm /dev/sdn /dev/sdo', u'raidz2 /dev/sdp /dev/sdq /dev/sdr /dev/sds /dev/sdt /dev/sdu /dev/sdv', u'spare /dev/sdw'], u'state': u'present', u'action': u'create', u'type': u'basic', u'options': [u'-f'], u'name': u'tank'})
[DEPRECATION WARNING]: Passing zfs properties as arbitrary parameters to the 
zfs module is deprecated.  Send them as a dictionary in the 
extra_zfs_properties parameter instead.. This feature will be removed in 
version 2.9. Deprecation warnings can be disabled by setting 
deprecation_warnings=False in ansible.cfg.

```

### Allow for variable number of Virtual HDD's in Vargantfile

* [](http://cobbaut.blogspot.ca/2014/04/vagrant-creating-10-vms-with-6-disks.html)


