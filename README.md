To verify that your User Data script ran successfully and that Kubernetes is ready to form a cluster, you need to check the installation logs, the service states, and the component versions.

sudo cat /var/log/cloud-init-output.log | grep -E "kubeadm|kubelet|kubectl|containerd"

systemctl status containerd

sudo containerd config dump | grep SystemdCgroup (It must output SystemdCgroup = true)

systemctl status kubelet

kubeadm version

kubectl version --client



