# Data Science development environment repository

Created based on: https://towardsdatascience.com/creating-a-solid-data-science-development-environment-60df14ce3a34

Utilizes Conda, Git, JupyterLab, AWS and DVC Tooling.

DVC is a data version control tool that integrates with git to track changes to data over time (https://dvc.org/). In this example, we create an AWS s3 bucket, download a file from s3://nasanex/LOCA on the aws registry of open data (https://registry.opendata.aws/nasanex/; documentation: https://docs.opendata.aws/nasa-nex/readme.html).

To replicate in local environment:

1. git clone https://github.com/lmenko917/DataDev_Pipeline.git

2. cd DataDev_Pipeline/

3. conda env create --file=datascience_devenv.yaml

4. conda activate datascience_devenv

5. ipython kernel install --user --name=datascience_devenv

6. dvc remote add -d sample_data s3://dvc-ds-devenv-test

7. dvc pull
