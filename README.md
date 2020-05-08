# kubernetes-elk-kibana-filebeat
In the old days, all components of your infrastructure were well-defined and well-documented. For example, a typical web application could be hosted on a web server and a database server.

sudo apt update

ls

sudo apt-get install docker.io

sudo usermod -aG docker $USER

sudo systemctl start docker

sudo systemctl enable docker

curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add

sudo apt-get install curl -y

sudo apt-add-repository "deb http://apt.kubernetes.io/ kubernetes-xenial main"

sudo apt-get install kubeadm kubelet kubectl -y

sudo hostnamectl set-hostname kmaster

ifconfig

sudo nano /etc/hosts

sudo swapoff -a

sudo nano /etc/fstab

Then create cluster

sudo kubeadm init --pod-network-cidr=10.244.0.0/16

mkdir -p $HOME/.kube

sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config

sudo chown $(id -u):$(id -g) $HOME/.kube/config

Create Network install for pods

sudo kubectl apply -f https://raw.githubusercontent.com/coreos/flannel/master/Documentation/kube-flannel.yml

Give Permission to access network and access

kubectl taint nodes  kmaster node-role.kubernetes.io/master-

kubectl apply -f rbac.yml

refer:-  https://www.magalix.com/blog/kubernetes-observability-log-aggregation-using-elk-stack
