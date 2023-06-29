# Awesome AI Environment

AI research relies much on learning codes written by other experienced researchers. However, many of open-source codes requires divergent environments. The environment configuration files inside are usually too strict to be compatible with each other. In this repo, we build a general conda environment that can cover as much repositories as possible.

## We wish you can contribute
Feel free to experiment with other repos, and pull requests.
- Set up a conda environment the same as us.
- Check if other repos can run directly. If not, try make minimal changes on existing packages.
- Provide short guidance. This is especially important if the pipeline under our env is different from the official tutorial.

## Repos We Support
### [Detectron2](https://github.com/facebookresearch/detectron2)
Detectron has been installed in an editable way. You may edit and import it following official instructions.
### [Detrex](https://github.com/IDEA-Research/detrex)
We consider Detrex as a code project, and would not link it to `site-packages`. Therefore, the following example codes only ensures that you can run detrex inside the folder.
```
git clone https://github.com/IDEA-Research/detrex.git
cd detrex
python setup.py build_ext --inplace
```
### [ODISE](https://github.com/NVlabs/ODISE)
We consider ODISE as a code project, and would not compile and link it to `site-packages`. Therefore, the following example codes only ensures that you can run ODISE inside the folder.
```
git clone https://github.com/NVlabs/ODISE.git
cd ODISE
PYTHONPATH=/path/to/repo:$PYTHONPATH 
```
### [TaskMatrix](https://github.com/microsoft/TaskMatrix)
### [DragGAN](https://github.com/XingangPan/DragGAN)
### [Obj2Seq](https://github.com/CASIA-IVA-Lab/Obj2Seq)

## Environment Setup

```
conda env create -f conda_env.yaml
conda activate awesome_env
pip install -r requirements.txt
pip install -r req_no_deps.txt --no-deps

# install the latest version of detectron2
git clone https://github.com/facebookresearch/detectron2.git
python -m pip install -e detectron2

# install maskformer
git clone https://github.com/NVlabs/ODISE.git
pip install panopticapi@https://github.com/cocodataset/panopticapi/archive/master.zip
pip install ODISE/third_party/mask2former --no-deps
# we take the env above, the official one from https://github.com/facebookresearch/Mask2Former.git has not been validated
```
- *Chinese users may refer [here](https://blog.51cto.com/u_15966109/6082769) for faster installations with mirror source.*
