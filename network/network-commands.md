# Host network links and its status
ip link

# Host network address
ip addr

# Host gateway display
ip route show default

# Mac address of another machine
arp node01
Address                  HWtype  HWaddress           Flags Mask            Iface
node01                   ether   02:42:ac:11:00:09   C                     ens3

# Active Internet connections (only servers)
netstat -nplt

# CNI location
/var/cni.d

# Pod's IP Block
kubectl logs weave-net-58ppk -c weave -n kube-system | grep ipalloc-range

# Cluster IP Block
cat /etc/kubernetes/manifests/kube-apiserver.yaml | grep cluster-ip-range