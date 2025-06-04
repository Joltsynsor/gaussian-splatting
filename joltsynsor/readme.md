# Env Set-up
## Training

Please see [local setup](../README.md#local-setup)

Set-up step-by-step

```bash
sudo apt-get update
# colmap
# do not use "sudo apt-get install colmap"
conda install -c conda-forge colmap
# imagemagick
# do not use "sudo apt-get install imagemagick"
conda install -c conda-forge imagemagick
# python env
cd **root directory**
conda env list | grep pytorch  # check pytroch exists
conda create --name 3dgs_env --clone pytorch
conda activate 3dgs_env
pip install -r joltsynsor/requirements.txt
```

# Training

## Pre-requests

### Rigid
1. Multi-view RGB images and camera parameters(both intrinsics and extrinsics).

### Optional
1. Point cloud

## Steps

### Metadata check

### transforms.json construction

### dataset construction
```text
<location>
|---images
|   |---<image 0>
|   |---<image 1>
|   |---...
|---sparse
    |---0
        |---cameras.bin
        |---images.bin
        |---points3D.bin
```






