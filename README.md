# Ansible kubernetes install on Centos 7

Run script to setup dependency in all host, then setup on master then node with command

`ansible-playbook  kubernetes.yaml  -i inventory.yaml`

`ansible-playbook  master.yaml  -i inventory.yaml`

`ansible-playbook  node.yaml  -i inventory.yaml`


Check in Master `$HOME` make sure file `cluster_init.txt` and `pod_network_setup.txt` is not exist

```
rm -rf ~/cluster_init.txt 
rm -rf ~/pod_network_setup.txt
rm -rf ~/.kube
```

Check in Node `$HOME` file `file node_joined.txt` is not exist

`rm -rf ~/cluster_init.txt`


Check cluster with command 

`kubectl get node`

Check pod with command

`kubectl get pods -n kube-system -o wide`
