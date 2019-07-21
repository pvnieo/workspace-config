
# server-config

## Install CUDA & Deep Learning Libraries

 - Uninstall old version CUDA Toolkit such as:
 ```
sudo apt-get purge cuda
sudo apt-get purge libcudnn6
sudo apt-get purge libcudnn6-dev
```
 - Install CUDA Toolkit 10 and cuDNN 7.0 as follows:
```
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-repo-ubuntu1804_10.0.130-1_amd64.deb
sudo dpkg -i cuda-repo-ubuntu1804_10.0.130-1_amd64.deb
sudo apt-key adv --fetch-keys https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/7fa2af80.pub
sudo apt-get update
wget http://developer.download.nvidia.com/compute/machine-learning/repos/ubuntu1804/x86_64/nvidia-machine-learning-repo-ubuntu1804_1.0.0-1_amd64.deb
sudo apt install ./nvidia-machine-learning-repo-ubuntu1804_1.0.0-1_amd64.deb
sudo apt-get update
sudo apt-get install --no-install-recommends nvidia-driver-418
```
 - Reboot. Check that GPUs are visible using the command: nvidia-smi
 - Install development and runtime libraries (~4GB)
 ```
sudo apt-get install --no-install-recommends cuda-10-0  libcudnn7=7.6.0.64-1+cuda10.0  libcudnn7-dev=7.6.0.64-1+cuda10.0
```
 - Install TensorRT. Requires that libcudnn7 is installed above.
```
sudo apt-get update
sudo apt-get install -y --no-install-recommends libnvinfer-dev=5.1.5-1+cuda10.0
```
 - Install Python3
 ```
 sudo apt-get update
sudo apt-get -y install python3-pip
export LC_ALL=C
```
 - Install TensorFlow & Pytorch
 ```
pip3 install tensorflow-gpu
pip3 install https://download.pytorch.org/whl/cu100/torch-1.1.0-cp36-cp36m-linux_x86_64.whl  
pip3 install https://download.pytorch.org/whl/cu100/torchvision-0.3.0-cp36-cp36m-linux_x86_64.whl
```
