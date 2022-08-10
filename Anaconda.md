# New environment
Create a new environment without requirements.txt file

`conda create -n env_name python=3.9 anaconda`
It  will install majority of what you need for data analysis work because of the `anaconda` part at the end. 

To activate the newly created environment

`conda activate env_name`

to deactivate

`conda deactivate`

To install a package, google search `conda + package_name` to find the appropriate code

## New environment with requirements.txt file. 

Go through the process above to create a new environment. After the environment is activated, run

`pip install -r requirements.txt`

# Conda Environments

List conda environments

`conda info --envs`. OR.
`conda env list`. ... 

# Update Anaconda

Code to update anaconda

`conda update -n base conda`

# Anaconda Navigator

Install anaconda navigator -- `conda install anaconda-navigator`

Uninstall Anaconda navigator -- `conda remove anaconda-navigator`
