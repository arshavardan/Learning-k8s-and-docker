**PV and PVC**
PV: persistantVolume it is specified with storage capacity that needs to be allocated.
PVC: it is provided within the podfile sometimes such that it is associated with that particular pod.
From the file below we can see that pvc is attached to a pod file with volumes attribute, and we can also see volume mounts in the same file where the path is 
provided within the container and this path is mapped locally to the path provided in the PV.
the pv and pvc is binded automatically once the accessmodes and storage matches with each other, provided within both the pv and pvc.
It's worth noting that a PersistentVolumeClaim can only be bound to a single PersistentVolume at a time, but a PersistentVolume can be bound to 
multiple PersistentVolumeClaims, as long as the accessModes, storageClassName, and capacity requirements are met.

**Hostpath**
if u want to create a volume such a way that u want the data is stored on both pods and available locally, for example the path in 
pod = /etc/pathinpod/ ;
local= /etc/pathlocally/ #localhost path
for this kind of scenario we can use HOSTPATH volume type

