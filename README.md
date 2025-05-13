# 2025-04-15-QCIF-Regression-Jupyter
 
This repository contains the set of Jupyter notebooks used to deliver the *Introduction to Regression for Machine Learning* workshop, online to the National Compute Infrastructure (NCI) on 15th April, 2025 and run on their Jupyter notebook system via the NCI Portal [are.nci.org.au](https://are.nci.org.au/)

The workbooks have been exported as PDF and are available in the [pdf](./pdf) directory. 

There are a set of images used for workbook *07_regression_maci_image_data.ipynb* in the ```./data``` directory  
which are published under the creative commons license terms Attribution-ShareAlike 4.0 (https://creativecommons.org/licenses/by-sa/4.0/)

### How-to setup a Jupyter server
TO execute the code in the Jupyter workbooks they must be run on a Jupyter server.  
The following instructions install the same libraries as used in for the tutorial session.  
The procedure uses a Python virtual environment and then registers the virtual environment with the 
Juypter server. A similar proceedure can be used in an NCI project account or on a laptop.

  N.B. make sure the ```<path/to>``` value is set to where your virtual environment has been created.
```shell
# Create a Python virtual environment:
python3 -m venv venv_regression

# Activate the virtual environment
source venv_regression/bin/activate  # On macOS/Linux, different on Windows: .venv\Scripts\activate

# Install packages
pip install jupyter ipykernel ipywidgets cmdstanpy[all] jupyter numpy scikit-learn pandas matplotlib statsmodels bokeh

# Install a ipython kernel configuration (change the value of --prefix= to match where your venv directory is)
python3 -m ipykernel install --prefix=<path/to>/venv_regression  --name=venv_regression --display-name "Python (venv_regression)"

# Start Jupyter Notebook Server
# Use the NCI Portal (https://are.nci.org.au/) and specify your new environment in the *Advanced* section of the JupyterLab featured app.
# or, Launch on your own system:
jupyter notebook
# Open the returned link in a web browser and load a workbook of your choice.
```

### Further resources for linear regression
Some videos of notes of Linear regression, where the calculations being described in the Jupyter notebooks are presented with audio descriptions.

[Linear Regression (YouTube)](https://www.youtube.com/watch?v=c7wYnbFaOnU)  
[Multiple Linear Regression (YouTube)](https://youtu.be/RcB_jOvVIaY)
