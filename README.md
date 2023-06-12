# Setup

```bash
conda create --name kws
conda activate kws

sudo apt install ffmpeg
pip3 install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
pip jupyter jupyterlab ipywidgets==7.6.5 install numpy ipython gradio ipywebrtc notebook
jupyter labextension install jupyter-webrtc 

```