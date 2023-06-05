# Diffusion-Tools
This repo contains tools and instructions to run several diffusion-related codes.

## Environment

```
conda env create -f diffusion_env.yaml
conda activate diffusion
pip install -r requirements.txt --no-deps
pip install -r detectron_req.txt

# install the latest version of detectron2
git clone https://github.com/facebookresearch/detectron2.git
python -m pip install -e detectron2

# install maskformer
git clone https://github.com/NVlabs/ODISE.git
pip install ODISE/third_party/mask2former
# we take the env above, you may also choose the official one from https://github.com/facebookresearch/Mask2Former.git


```

- *The `conda` command may take an extremely long time to finish without anything printed on the screen. If you want to see the pip progress. Copy the pip part as a separate requirements file and execute it.*
- *Chinese users may refer [here](https://blog.51cto.com/u_15966109/6082769) for faster installations with mirror source.*
