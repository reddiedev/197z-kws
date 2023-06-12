# EEE 197z Project 2 - Zero-Shot KWS using ImageBind
an algorithm using ImageBind that will classify KWS test dataset (Google Speech Commands v2 35) in zero-shot manner. 

*Author: Sean Red Mendoza | 2020-01751 | scmendoza5@up.edu.ph*

## Tools/ References
- [ImageBind](https://github.com/facebookresearch/ImageBind)
- [Gradio](https://gradio.app/)
- [roatienza/Deep-Learning-Experiments](https://github.com/roatienza/Deep-Learning-Experiments)
- [Google Cloud G2 GPU VM (2x Nvidia L4)](https://cloud.google.com/blog/products/compute/introducing-g2-vms-with-nvidia-l4-gpus)

## Goals
- [x] randomly pick an audio from the test split and classify it (audio player in UI)
- [x] user should be able to record his/her own voice for testing (audio recorder in UI, powered by Gradio)
- [x] show summary statistics during evaluation of n sampels (# of data points, accuracy).
- [x] comparison table of SOTA model scores

# Usage

1. Duplicate this repository on a working directory
```bash
git clone https://github.com/reddiedev/197z-kws
cd 197z-kws
```

2. Prepare environment for running the notebook

```bash
conda create --name kws
conda activate kws

sudo apt install ffmpeg

pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
pip jupyter jupyterlab ipywidgets==7.6.5 install numpy ipython gradio ipywebrtc notebook

jupyter labextension install jupyter-webrtc 

```

3. Run the `demo.ipynb` jupyter notebook

# Acknowledgements
[Professor, Rowel Atienza](https://github.com/roatienza)