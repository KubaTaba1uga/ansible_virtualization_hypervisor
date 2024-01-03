# Manage Virtualization Hypervisor via ansible

Create virtualized environment that mimic home network with just one command.

## Network Architecture
![Network architecture](/network.png) 

## Prepare environment
```
pip install -r requirements.txt
```
```
ansible-galaxy collection install community.libvirt
ansible-galaxy collection install community.general
```

## Configure environment
```
ansible-playbook -i <ip>, set-up.yml -u <username>
```

Example:
```
ansible-playbook -i 10.0.0.26, set-up.yml -u user
```

## Create VM
```
ansible-playbook -i <ip>, create-vm.yml -u <username> -e vm_name=<vm_name>
```

Example:
```
ansible-playbook -i 10.0.0.26, create-vm.yml -u user -e vm_name=vm0
```

## Delete VM
```
ansible-playbook -i <ip>, delete-vm.yml -u <username> -e vm_name=<vm_name>
```

Example:
```
ansible-playbook -i 10.0.0.26, delete-up.yml -u user -e vm_name=vm0
```

