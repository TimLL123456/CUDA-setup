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
