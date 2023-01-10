## Notes for setting up conda environment - Including installing Ipykernel

#### Creating a conda environment
    conda create -n <env_name> python=<python_version>

(reference: https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)

 #### Installing and setting up Ipykernel
 
    conda install ipykernel # or pip install ipykernel
    python -m ipykernel install --user --name <env_name> --display-name "<env_display_name>"

(reference: https://ipython.readthedocs.io/en/stable/install/kernel_install.html)
