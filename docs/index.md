# NEORICALEX

Em desenvolvimento ...


# Py
sudo apt install python3-pip -y
sudo pip3 install virtualenv 
virtualenv env
source env/bin/activate

# MK Docs
pip install mkdocs
mkdocs new .

# KVM
egrep -c '(vmx|svm)' /proc/cpuinfo
sudo apt install qemu-kvm libvirt-clients libvirt-daemon-system bridge-utils -y
sudo adduser $USER libvirt
sudo adduser $USER kvm
sudo apt install virt-manager -y

# SystemBack - GUI para criar ISO
sudo apt install systemback -y


