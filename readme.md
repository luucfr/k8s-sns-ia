## INSTALLATION DRIVER NVIDIA
```
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2404/x86_64/cuda-keyring_1.1-1_all.deb
sudo dpkg -i cuda-keyring_1.1-1_all.deb
sudo apt-get update
sudo apt-get -y install cuda-toolkit-12-8

sudo apt-get install -y cuda-drivers
reboot
sudo apt-get install -y nvidia-container-toolkit
```

### VERIFICATION
```
nvidia-smi
```
Si des cartes sont afficher driver OK

## INSTALLATION runc
```
sudo apt-get install -y runc
```

### APPLICATION DU DEAMON NVIDIA DANS K3S
```
cd nvidia-runtime\

kubectl apply -f deamonset-nvidia.yaml
kubectl apply -f nvidia-runtimeclass.yaml

kubectl label nodes sns-ia-01 workload=ai
kubectl label nodes sns-ia-02 workload=ai
```