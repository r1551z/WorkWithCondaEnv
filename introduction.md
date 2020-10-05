


# step 0:

open anaconda prompt

# step 1: create / activate / deactivate / remove your conda virtual environment

```
conda create -n myenv python=3.7
conda activate myenv
conda deactivate  
conda remove -n myenv --all
```

# step 2: install ipykernal and register it to your jupyter notebook.

```
$ conda activate cenv

(myenv)$ conda install ipykernel

(myenv)$ ipython kernel install --user --name=tfcpu

(myenv($ conda deactivate
```
Ref: https://stackoverflow.com/questions/37433363/link-conda-environment-with-jupyter-notebook

Looks like if you are using virualenv the above step will be all good.

Unfortunately I'm not using that, so I need to register the kernel so my jupyter notebook can understand it.

# step 3: launch jupyter notebook

```
cd <your target file location>
jupyter notebook
```
When I did that for the first time I was told jupyter notebook is not recognized so I reinstalled jupyter notebook
inside my conda environment

```
pip install jupyter notebook
```
# step 4: open your jupyter notebook

Open your target jupyter notebook, click on 'kernal', and choose 'tfcpu' -- the one you created in step 2.

# step 5: check the python path.
```python
import sys
sys.executable
```
If the location is shown as the python in your virtual environment, now you are all good to go!

# some other tips:
Here are some other commands you probably will find useful.
Show all current virtual environments
```
conda env list
```
Create a new environmeny myclone by cloning myenv
```
conda create --name< myclone> --clone <myenv>
```
See all packages in my env
```
conda list -n myenv
```
Remove an environment
```
conda remove --name myenv --all
```
