# ROADMAP.md

## Notes

### Creating a variable amount of Virtual HDD's using the Vargantfile

* [](http://cobbaut.blogspot.ca/2014/04/vagrant-creating-10-vms-with-6-disks.html)


```shell
(1..8).each do |i|
  vbox.customize ['createhd', '--filename', "server_#{i}a.vdi", '--size', 8192 ]
#  vbox.customize ['createhd', '--filename', "server_#{i}b.vdi", '--size', 8192 ]
  vbox.customize ['storageattach', :id, '--storagectl', 'SATA', '--port', 1, '--device', 0, '--type', 'hdd', '--medium', "./server_#{i}a.vdi"]
#  vbox.customize ['storageattach', :id, '--storagectl', 'SATA', '--port', 2, '--device', 0, '--type', 'hdd', '--medium', "./server_#{i}b.vdi"]
end
```
