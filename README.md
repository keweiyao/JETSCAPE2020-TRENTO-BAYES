# JETSCAPE2020-TRENTO-BAYES

## Prerequisite and Installation

These examples run with `python3` on a `Jupyter Notebook`. 
We provided two options to either install the dependencies using [Anaconda](https://www.anaconda.com/) or simply run the code from an online session supported by [Binder](https://mybinder.org/).

### Option 1. Conda virtual environment (recommended)

1. Download `Miniconda` (a free minimal version of Anaconda) for Python 3.7 from [here](https://docs.conda.io/en/latest/miniconda.html). Remember to choose `Python3` (3.7) and the correction installer for your operating system.
2. Execute the downloaded installer, and follow the instructions to install.
It will ask you where to put conda (Default is `$HOME`). After the installation, `conda` command can be called in shell (for Mac / Linux). For Windows, you can find `anaconda prompt` from your start menu to open a shell environment.
3. Clone the current repository to a directory, for example `$HOME/JS2020`.
```
mkdir $HOME/JS2020 && cd $HOME/JS2020 git clone https://github.com/keweiyao/JETSCAPE2020-TRENTO-BAYES.git 
```
Using the script `postBuild` to down the date files  
```
cd $HOME/JS2020/JETSCAPE2020-TRENTO-BAYES 
bash postBuild 
```
4. Create conda virtual environment.
```
conda env create -f conda-environ.yml 
```
This should create a virtual environment called `trento-bayes`. You can check if it exists and its location by `conda env list`. The required libraries are installed in this environment (these libraries are listed in `environment.yml`, except for `emcee` package). If you want to delete this environment after the lecture, you can do `conda env remove -n <name-of-environment>`.
5. To activate the environment 
```
conda activate trento-bayes 
```
To deactivate the environment 
```
conda deactivate 
```
6. Activate the environment, and install the `emcee` package for MCMC using `pip` command 
```
pip install emcee 
```
7. Within the folder that contains the examples, open jupyter notebook, 
```
jupyter notebook 
```
From the prompt of the browser, click and open the file `trento-bayes.ipynb`
8. Move to the first block, press `Shift+Enter` to see if you can run the first two or three blocks successfully. 
Then you are good to go!

### Option 2. Using online Binder environment

This Binder environment holds online session of interactive `Jupyter notebook`. 
Simple check the following link and wait for the environment to build and load.
[Binder link](https://mybinder.org/v2/gh/keweiyao/JETSCAPE2020-TRENTO-BAYES/master ).
The advantage is that you don't need to install the dependence on your computer. 
The disadvantages: the computational power of the binder server is limited. 
So for some examples with significant amount of computation, it will be too long for the lecture. 
Therefore, I also uploaded pre-calculated results for these examples that you can simply load and study.
Another disadvantage is that if your internet connection is unstable, sometimes you need to restart the server again.
