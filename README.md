How To Run this github Repo "https://github.com/DarlingHang/st-nerf" on Windows Desktop Step By Step

### Installation
first create a folder on destop where you want to clone the repository and then open the cmd(command prompt in newly created folder and than copy this code
- Clone this repo: 
```bash
git clone https://github.com/DarlingHang/st-nerf


```
first Install the python 3.8.5 version on the destop
-To run this code firse we have to create a virtual environment and all the dependencies to run the code


```
pip install virtualenv
virtualenv myenv
myenv\Scripts\activate
```
BEFORE download all the dependencies first download the nvidia cudatoolkit11.0 from "https://developer.nvidia.com/cuda-11.0-download-archive"
Now download all dependencies
```
pip install torch==1.7.1+cu110 torchvision==0.8.2+cu110 torchaudio==0.7.2 -f https://download.pytorch.org/whl/torch_stable.html
pip install imageio matplotlib
pip install install yacs kornia robpy
```
check all the virson correctly from requirment file
'''
aiohttp==3.8.1
aiosignal==1.2.0
anyio==3.6.1
argon2-cffi==21.3.0
argon2-cffi-bindings==21.2.0
asttokens==2.0.5
async-timeout==4.0.2
attrs==21.4.0
Babel==2.10.3
backcall==0.2.0
beautifulsoup4==4.11.1
bleach==5.0.1
certifi==2022.6.15
cffi==1.15.1
charset-normalizer==2.1.0
colorama==0.4.5
cycler==0.11.0
debugpy==1.6.2
decorator==5.1.1
defusedxml==0.7.1
deprecation==2.1.0
entrypoints==0.4
executing==0.8.3
fastjsonschema==2.15.3
fonttools==4.34.4
freetype-py==2.3.0
frozenlist==1.3.0
idna==3.3
imageio==2.19.3
imageio-ffmpeg==0.4.7
importlib-metadata==4.12.0
importlib-resources==5.8.0
ipykernel==6.15.1
ipython==8.4.0
ipython-genutils==0.2.0
ipywidgets==7.7.1
jedi==0.18.1
Jinja2==3.1.2
json5==0.9.8
jsonschema==4.7.2
jupyter-client==7.3.4
jupyter-core==4.11.1
jupyter-packaging==0.12.2
jupyter-server==1.18.1
jupyterlab==3.4.3
jupyterlab-pygments==0.2.2
jupyterlab-server==2.15.0
jupyterlab-widgets==1.1.1
kiwisolver==1.4.4
kornia==0.5.11
MarkupSafe==2.1.1
matplotlib==3.5.2
matplotlib-inline==0.1.3
mistune==0.8.4
multidict==6.0.2
nbclassic==0.4.3
nbclient==0.6.6
nbconvert==6.5.0
nbformat==5.4.0
nest-asyncio==1.5.5
networkx==2.8.4
notebook==6.4.12
notebook-shim==0.1.0
numpy==1.23.1
open3d==0.15.1
packaging==21.3
pandocfilters==1.5.0
parso==0.8.3
pickleshare==0.7.5
Pillow==9.2.0
prometheus-client==0.14.1
prompt-toolkit==3.0.30
psutil==5.9.1
pure-eval==0.2.2
pycparser==2.21
pyglet==1.5.26
Pygments==2.12.0
PyOpenGL==3.1.0
pyparsing==3.0.9
pyrender==0.1.45
pyrsistent==0.18.1
python-dateutil==2.8.2
pytz==2022.1
pywin32==304
pywinpty==2.0.6
PyYAML==6.0
pyzmq==23.2.0
requests==2.28.1
robopy==1.0.8
robotframework==5.0.1
robpy==0.1
scipy==1.8.1
Send2Trash==1.8.0
six==1.16.0
sniffio==1.2.0
soupsieve==2.3.2.post1
stack-data==0.3.0
terminado==0.15.0
tinycss2==1.1.1
tomlkit==0.11.1
torch==1.7.1+cu110
torchaudio==0.7.2
torchvision==0.8.2+cu110
tornado==6.2
traitlets==5.3.0
trimesh==3.12.8
typing_extensions==4.3.0
urllib3==1.26.10
vtk==9.1.0
wcwidth==0.2.5
webencodings==0.5.1
websocket-client==1.3.3
widgetsnbextension==3.6.1
wslink==1.6.6
yacs==0.1.8
yarl==1.7.2
zipp==3.8.1

'''






### Datasets
The walking and taekwondo datasets can be downloaded from [here](https://drive.google.com/drive/folders/13YHw_YSGewvcgYdwqbelM9L2JiPNWLi7?usp=sharing).

### Apply a pre-trained model to render demo videos
- We provide our pretrained models which can be found under the `outputs` folder.
- We provide some example scripts under the `demo` folder.
- To run our demo scripts, you need to first downloaded the corresponding dataset, and put them under the folder specified by `DATASETS` -> `TRAIN` in `configs/config_taekwondo.yml` and `configs/config_walking.yml`
- For the walking sequence, you can render videos where some performers are hided by typing the command:
```
python demo/walking_demo.py -c configs/config_walking.yml
```
- For the taekwondo sequence, you can render videos where performers are translated and scaled by typing the command:
```
python demo/taekwondo_demo.py -c configs/config_taekwondo.yml
```
- The rendered images and videos will be under `outputs/taekwondo/rendered` and `outputs/walking/rendered`

