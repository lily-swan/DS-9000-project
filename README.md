# DATASCI 9000: Machine Learning Project

We're attempting to build a classifier to work with Kepler's exoplanet data. Our aim is to make it easier to classify exoplanets.

__Dataset__: https://www.kaggle.com/datasets/nasa/kepler-exoplanet-search-results


## Setup

### Linux and Mac
1. Make sure you have `virtualenv` installed.
    ```
    pip install virtualenv
    ```
2. (Optional) Download an API token from Kaggle.
3. In the same folder as this repo, run the following to create the virtualenv, activate it, and install the necessary packages:
    ```
    virtualenv --python /usr/bin/python3.10 .venv

    # Activate venv and install dependencies
    source .venv/bin/activate
    pip install -r requirements.txt

    # Download data-- assumes kaggle.json exists at ~/.kaggle/kaggle.json
    kaggle datasets download nasa/kepler-exoplanet-search-results -f cumulative.csv
    ```
    Note that if you don't want to use the kaggle CLI to download data, you can skip the last line and just download it manually.
4. Start your jupyter server. I just use vscode, but jupyter has been included so you can run your own server if you'd like.

### Windows
These steps haven't been tested.
1. Create a new conda environment
    ```
    conda create --name .venv python=3.10
    ```
2. (Optional) Download an API token from Kaggle.
3. Activate the conda environment and install all necessary packages.
    ```
    conda activate .venv
    conda install --yes --file requirements.txt
    ```
4. Start your jupyter server.