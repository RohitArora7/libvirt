# libvirt
```bash
installtion
sudo apt install -y qemu qemu-kvm libvirt-daemon libvirt-clients bridge-utils virt-manager

check status
sudo systemctl status libvirtd

enable systemboot
sudo systemctl enable --now libvirtd

check status for virtualization 
egrep -c '(vmx|svm)' /proc/cpuinfo
lsmod | grep -i kvm
sudo apt install cpu-checker
sudo kvm-ok


/var/lib/libvirt/images/


virsh list --all

sudo virsh domifaddr amcop-vm-01

virsh start amcop-vm-01 

virsh shutdown amcop-vm-01 

virsh undefine  amcop-vm-01 
#get location
sudo virsh domblklist ubuntu20.04-k8s-try-emco-67
#get info
sudo qemu-img info /var/lib/libvirt/images/ubuntu20.04-k8s-try-emco-67.qcow2
#view all snapshot
sudo virsh snapshot-list ubuntu20.04-k8s-try-emco-67


The qemu package (quick emulator) is an application that allows you to perform hardware virtualization.
The qemu-kvm package is the main KVM package.
The libvritd-daemon is the virtualization daemon.
The bridge-utils package helps you create a bridge connection to allow other users to access a virtual machine other than the host system.
The virt-manager is an application for managing virtual machines through a graphical user interface.
```
