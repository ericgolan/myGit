set GOVC_INSECURE=True
set GOVC_URL=vcenter.harel.lab
set GOVC_USERNAME=administrator@vsphere.local
set GOVC_PASSWORD=P@ssw0rd

# list all folders in the Folder view 
govc ls /Datacenter/vm
# create a folder under the vm folder - used for placing VM's 
govc folder.create /Datacenter/vm/GolanLAB

# get all VM options for creating a vm
govc vm.option

