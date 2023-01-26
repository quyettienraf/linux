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
Done, now just source the bashrc file again to load the changes
```bash
source ~/.bashrc
```
- step 3: verify
- download Cuda Sample: https://github.com/NVIDIA/cuda-samples
```bash
$ cd <sample_dir>
$ make
$ ./bandwidthTest 
```
### install cudnn 

Just go [here](https://developer.nvidia.com/cudnn) and follow the [instructions](https://docs.nvidia.com/deeplearning/sdk/cudnn-install/index.html). You'll have to log in, so downloading of the right cuDNN binary packages cannot be easily automated. Meh.

Once downloaded, un-tar the file and copy the contents to their respective locations:

    $ tar -xzvf cudnn-11.0-linux-x64-v8.0.2.39.tgz
    
    $ sudo cp cuda/include/cudnn*.h /usr/local/cuda/include
    $ sudo cp cuda/lib64/libcudnn* /usr/local/cuda/lib64
    $ sudo chmod a+r /usr/local/cuda/include/cudnn*.h /usr/local/cuda/lib64/libcudnn*
