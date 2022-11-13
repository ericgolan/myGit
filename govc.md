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

#get all Datastore info from cluster
govc datastore.info

# List all Portgroup on Hosts
host.portgroup.info

#create a VM # note ISO should be in the root of the datastore 
govc vm.create -ds=/Datacenter/datastore/Netapp_nfs_Datastore02 -net=Management -g rhel8_64Guest -c 4 -m 8192 -disk=100g -on=false -iso-datastore=Netapp_nfs_Datastore01 -iso=Rocky-9.0-20220805.0-x86_64-minimal.iso  GolanMainVM

