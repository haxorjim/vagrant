# vagrant

```
boxes="win7-ie9 win7-ie10 win7-ie11"
for box in $boxes; do
    vagrant box add --clean modernIE/$box http://aka.ms/vagrant-$box
done

wget https://az792536.vo.msecnd.net/vms/VMBuild_20160810/Vagrant/MSEdge/MSEdge.Win10_RS1.Vagrant.zip
unzip MSEdge.Win10_RS1.Vagrant.zip
vagrant box add --clean modernIE/win10-edge dev-msedge.box
rm MSEdge.Win10_RS1.Vagrant.zip
rm win10-edge dev-msedge.box
```

# provisioning

1. Mark Networks as Work, not Public.
2. Disable Firewall.
3. Install Java.
4. Setup winrm.bat to run at startup.
5. Setup selenium.bat to run at startup.
