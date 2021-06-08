# Ansible kubernetes install on Centos 7

Run script with command

`ansible-playbook  kubernetes.yaml  -i inventory.yaml`


Check in `$HOME` make sure file `cluster_init.txt` and `pod_network_setup.txt` is not exist

```rm -rf ~/cluster_init.txt 
rm -rf ~/pod_network_setup.txt
rm -rf ~/.kube```

