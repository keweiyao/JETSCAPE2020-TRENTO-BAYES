# JETSCAPE2020-TRENTO-BAYES

## Pre-requisite and Installation

These examples runs with `python3` on a `Jupyter Notebook`. 
Please check [requirements.txt](requirements.txt).

We provided two options to install the dependences or run the code within an online session.

### Option 1. Conda virtual enviroment

1. Download Miniconda for Python 3.7 from [here](https://docs.conda.io/en/latest/miniconda.html)
2. Execute the downloaded installer, and follow the instructions. 
It will ask you where to put conda (Default is `$HOME`).
3. Clone the current repository to a directroy, for example `$HOME/JS2020`.

```
mkdir $HOME/JS2020 && cd $HOME/JS2020
git clone https://github.com/keweiyao/JETSCAPE2020-TRENTO-BAYES.git
```
Using the script postBuild to down the date files 
```
cd $HOME/JS2020/JETSCAPE2020-TRENTO-BAYES
bash postBuild
```

4. Create conda virtual enciroment.

```
conda env create -f environment.yml
```
This shoud create an virtual environment called `trento-bayes`. You can check if it exists and its location by `conda env list`. The required libraries are installed in this environment (these libraries are listed in `environment.yml`, except for `emcee` package). If you want to delete this environment after the lecture, you can do `conda env remove -n <name-of-environment>`.

5. To activate the environment

```
conda activate trento-bayes
```
To deactivate the enviornment
```
conda deactivate
```

6. Activate the enviroment, and install the `emcee` package for MCMC using `pip` command

```
pip install emcee
```

7. WIthin the folder that contains the examples, open jupyter notebook,
```
jupyter notebook
```
From the prompt of the browser, click and open the file `trento-bayes.ipynb`

8. Move to the first block, press `Shift+Enter` to see if you can run the first two or three blocks successfully. 
Then you are good to go!


### Option 2. Using online Binder environment

This Binder enviroment holds online session of interactive `Jupyter notebook`. 
Simple check the following link and wait for the envirnment to build and load.
[Binder link](https://mybinder.org/v2/gh/keweiyao/JETSCAPE2020-TRENTO-BAYES/master
).

The advantage is that you don't need to install the dependence on you computer. 
The disadvantages: the computational power of the binder server is limited. 
So for some examples with significant amount of computation, it will be too long for the lecture. 
Therefore, I also uploaded pre-calcualted results for these examples that you can simply load and study.
Another disadvantage is that is you internet connection is unstable, sometimes you need to restart the server again.

