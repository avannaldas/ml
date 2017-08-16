---
layout: post
title:  "Installing Tensorflow-GPU on Windows"
date: 2017-08-17
---

To use tensorflow library on GPU, NVIDIA CUDA Toolkit and cuDNN libraries need to be first installed. Installing `tensorflow-gpu` is straight forward. Installing the NVIDIA CUDA Toolkit and cuDNN is slightly tricky, we need to ensure a couple of things so that CUDA toolkit works that tensorflow-gpu uses under the hood.

Let's begin...

1. Download <A href="https://developer.nvidia.com/cuda-downloads" target="_blank">CUDA Toolkit 8.0</A> and <A href="https://developer.nvidia.com/cudnn" target="_blank">cuDNN v5.1 for CUDA Toolkit 8.0</A> from NVIDIA Developer portal

2. Install CUDA Toolkit 8.0
    * Sometimes if the GPU is a latest one, CUDA Toolkit may not have support for it. This shouldn't stop you from using CUDA Tookit, but the CUDA Toolkit installation warns that it couldn't find a compatible GPU Hardware. In that case, go for a custom installation and choose not to install the drivers. Should be easy to identify in the custom install screen.


3. Copy the contents of the cuDNN downloaded archive into CUDA Toolkit installed folder

4. Add below two paths to the system 'PATH' environment variable (if CUDA Toolkit installation didn't add it):
    * C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0\lib\x64
    * C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0\extras\CUPTI\libx64


5. Ensure below three environment variables are available with value _`C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v8.0`_ or wherever the CUDA toolkit is installed. Create the missing variables.
    * `CUDA_HOME` - this needs to be added manually
    * `CUDA_PATH` - this is usually created after installing CUDA Toolkit 8.0
    * `CUDA_PATH_V8_0` - this is usually created after installing CUDA Toolkit 8.0


6. Installing `tensorflow-gpu`
    * If tensorflow package without gpu support is installed, uninstall it.
    * Install tensorflow-gpu using `pip install tensorflow-gpu` OR `conda install tensorflow-gpu` (if using anaconda). If already installed, uninstall it and then reinstall. It didn't work for me until I reinstalled.


7. If `tflearn` is required, install it with one of the below commands
    * `pip install tflearn`
    * `conda install -c derickl tflearn`



You can find the official tensorflow documentation guide for tensorflow-gpu setup <A href="https://www.tensorflow.org/install/install_windows#requirements_to_run_tensorflow_with_gpu_support" target="_blank">here</A>.

