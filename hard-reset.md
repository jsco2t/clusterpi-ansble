# Resetting cluster and cluster nodes

## Remove required resources

sudo kubeadm reset -f
sudo apt purge -y kubeadm kubectl kubelet kubernetes-cni kube*
sudo apt autoremove -y
sudo rm -rf ~/.kube
sudo rm -rf /etc/cni /etc/kubernetes /var/lib/dockershim /var/lib/etcd /var/lib/kubelet /var/run/kubernetes /opt/cni/bin
sudo iptables -F && sudo iptables -t nat -F && sudo iptables -t mangle -F && sudo iptables -X
--sudo systemctl restart docker

## Packages that may need to be re-installed

sudo apt purge -y containerd.io docker-ce-cli docker-ce-rootless-extras docker-ce
sudo reboot
sudo rm -rf /etc/containerd
sudo apt install -y docker-ce
sudo apt install -y containerd.io
sudo apt install -y docker-ce-cli docker-ce-rootless-extras
sudo systemctl status docker