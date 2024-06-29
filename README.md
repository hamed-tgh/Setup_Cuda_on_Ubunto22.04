# Setup_Cuda_on_Ubunto22.04

In this file, I create a tutorial in order to Install Cuda on Ubunto 22.04

## 1) in ordert to Install Cuda, First you have to download cuda 12.1 from mentioned URL. <You'd better to download it in local>.

https://developer.nvidia.com/cuda-12-1-0-download-archive?target_os=Linux&target_arch=x86_64&Distribution=Ubuntu&target_version=22.04&target_type=runfile_local

## 2) To install GPU driver related to cuda 12.1 You have to install nvidia driver V.530 by using bellow command
suda apt install nvidia-driver-530

## 3) Rebbot

## 4) install Cuda 12.1 which is downloaded in step 1
### 4-1) *during install uncheck installing the Nvidia-530-driver*
sudo sh <name of Cuda being Downloaded.run>


## 5) Fix Problems
sudo apt --fix-broken install
sudo apt autoremove

## 6) Reboot

## 7) Add cuda to Path
nano ~./bashrc
./ ~/.bashrc

export PATH=/usr/local/cuda/bin${PATH:+:${PATH}}
export LD_LIBRARY_PATH=/usr/local/cuda-12.1/lib64\
                         ${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}

## 8) Test
nvcc -v

