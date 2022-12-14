# Merge-Stable-Diffusion-models-without-distortion
I wrote the permutation spec for Stable Diffusion necessary to merge with the git-re-basin method outlined here - https://github.com/samuela/git-re-basin.
This is based on a 3rd-party python implementation of that here - https://github.com/themrzmaster/git-re-basin-pytorch.

The results of a model merge have not been tested yet but I am done with the spec.
To merge, you will need to install pytorch 1.11.0 or lower (1.12.0 will not work). 

Download the code folder, open cmd in the directory, transfer the desired models to the same folder and run 
"python SD_rebasin_merge.py --model_a nameofmodela.ckpt --model_b nameofmodelb.ckpt"

If not in the same directory then 
pathofmodela.ckpt and pathofmodelb.ckpt instead

CPU + GPU works now

## Installation Windows

```powershell
python -m venv --system-site-packages venv
.\venv\Scripts\activate

pip install torch==1.11.0+cu113 torchvision==0.12.0+cu113 torchaudio==0.11.0 --extra-index-url https://download.pytorch.org/whl/cu113
pip install scipy easygui

```

## Running

`python SD_rebasin_merge.py --model_a nameofmodela.ckpt --model_b nameofmodelb.ckpt`