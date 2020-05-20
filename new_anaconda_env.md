To get the environment setup:

Open your command line tool (Terminal for MacOS, Anaconda Prompt for Windows)

Navigate to the folder with this sprint's content. There should be a requirements.txt

Run conda create -n U4-S2-NNF python==3.7 => You can also rename the environment if you would like. Once the command completes, your conda environment should be ready.

Now, we are going to add in the require python packages for this sprint. You will need to 'activate' the conda environment: source activate U4-S2-NNF on Terminal or conda activate U4-S2-NNF on Anaconda Prompt. Once your environment is activate, run pip install -r requirements.txt which will install the required packages into your environment.

We are going to also add an Ipython Kernel reference to your conda environment, so we can use it from JupyterLab.

Next run python -m ipykernel install --user --name U4-S2-NNF --display-name "U4-S2-NNF (Python3)" => This will add a json object to an ipython file, so JupterLab will know that it can use this isolated instance of Python. :)

Deactivate your conda environment and launch JupyterLab. You should know see "U4-S2-NNF (Python3)" in the list of available kernels on launch screen.