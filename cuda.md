### https://linuxhint.com/install-cuda-ubuntu-2004/
### 1. Install cuda toolkit
- step 1: install  
```bash
sudo apt install nvidia-cuda-toolkit
```
### https://gist.github.com/matheustguimaraes/43e0b65aa534db4df2918f835b9b361d
- step 2: upgrade
- https://gist.github.com/katnoria/671d37188340d351b2f9b459feb05b44
- updating cuda version
```bash
export PATH=/usr/local/cuda-10.0/bin:$PATH export LD_LIBRARY_PATH=/usr/local/cuda-10.0/lib64:$LD_LIBRARY_PATH
```
- step 3: verify
- download Cuda Sample: https://github.com/NVIDIA/cuda-samples
```bash
$ cd <sample_dir>
$ make
$ ./bandwidthTest 
```
