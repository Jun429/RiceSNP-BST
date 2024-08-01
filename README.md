**Automated Modeling for Biological Evidence-based Research**

<a id='sec1'></a>
RiceSNP-BST is a toolkit for designing high-performance neural network models automatically in
Genomics and Bioinformatics.

☆**RiceSNP-BST can be used to predict BST-associated SNPs:**
- 🟢 Data Collection and Processing
- 🟢 SHAP Feature Optimization
- 🟢 Automatic CNN Model Optimization
- 🟢 Benchmark Testing
- 🟢 User-Friendly interface

△**Supported backend deep-learning libraries:**
- 🟢 Tensorflow 1.X / Keras
- 🟢 Pytorch / Pytorch-Lightning
- 🟢 TensorFlow 2
---
## Table of Contents
1. [Installation](#sec2)
2. [Quick Start](#sec3)
3. [Contact & References](#sec4)


<a id='sec2'></a>
## Installation

Currently RiceSNP-BST is designed to be run in Unix-like environment. As a prerequisite, please make sure
 you have Anaconda/miniconda installed, as we provide the detailed dependencies through a conda 
 environment.
 

Please follow the steps below to install RiceSNP-BST. To install `RiceSNP-BST`, 
you can use `conda` and `pypi` to install a versioned release (recommended).

> NOTE:
We strongly encourage you to create a new conda environment, regardless of the backend library you choose.


### Installing with TF 1.X/Keras
In the command-line terminal, type the following commands to get it installed:

```{bash}
conda create -n amber-tf1 -c anaconda tensorflow-gpu=1.15.0 keras scikit-learn numpy~=1.18.5 h5py~=2.10.0 matplotlib seaborn
# if you don't have CUDA-enabled GPU, or on MacOS, replace tensorflow-gpu=1.15.0 with tensorflow=1.15.0
conda activate amber-tf1
pip install amber-automl
# if you plan to run tests
pip install pytest coverage parameterized pydot graphviz
```

### Installing with PyTorch/Lightning
```{bash}
conda create -n amber-torch -c conda-forge pytorch=1.11.0 scikit-learn numpy scipy matplotlib seaborn tqdm h5py
conda activate amber-torch
pip install pytorch-lightning==1.6.5 torchmetrics==0.11.0 amber-automl
# if you plan to run tests
pip install pytest coverage parameterized expecttest hypothesis
```

### Installing with Tensorflow 2
```{bash}
conda create -n amber-tf2 -c conda-forge tensorflow-gpu scikit-learn seaborn
# if you are on MacOS, or don't have CUDA-enabled GPU, replace tensorflow-gpu with tensorflow
conda activate amber-tf2
pip install pytorch-lightning==1.6.5 torchmetrics==0.11.0 amber-automl
# if you plan to run tests
pip install pytest coverage parameterized pydot graphviz
```

### Switching between Backends
```{bash}
amber-cli config --backend pytorch
```
### Testing your installation
You can test if RiceSNP-BST can be imported to your new `conda` environment by:

```bash
conda activate amber
amber-cli --version
```

If the version number is printed out, and no errors pop up, that means you have successfully installed RiceSNP-BST.

The typical installation process should take less than 10 minutes with regular network 
connection and hardware specifications. 

[Back to Top](#sec0)

