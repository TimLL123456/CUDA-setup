# cuda-torch-in-conda
Install cuda and pytorch in conda environment

# Create conda env
```
conda create -n pytorch python=3.10 cudatoolkit=11.8 uv -y
```

# PIP install requirements.txt with uv
**requirements.txt**
```
pandas
numpy
matplotlib

--extra-index-url https://download.pytorch.org/whl/cu118
torch
torchvision
torchaudio
```

```
uv pip install -r requirements.txt
```

# Change cuda version with update-alternatives
set symbolic link in **~/.bashrc**

```
export PATH=/usr/local/cuda/bin:$PATH
export CUDA_HOME=/usr/local/cuda
export LD_LIBRARY_PATH=/usr/local/cuda/lib64:$LD_LIBRARY_PATH
```
