## How to install
1.	Download and install the latest version of anaconda
    -	https://www.anaconda.com/products/individual 
2.	Open an anaconda prompt (found in windows menu), and enter the following commands:
    - `conda create --name pychEnv`
        - Enter `y` (for yes)
    -	`conda activate pychEnv`
    -	`conda install git pip ipykernel`
        - Enter `y` (for yes)
    -	`python -m ipykernel install --user --name pychEnv --display-name "Python (pychEnv)"`
    -	`pip install git+git://github.com/Nickp1993/Pych/`
    -	Close this window (do not continue with the "how to use" without closing!)
3.	You have finished installation, continue with the "How to use" below to start a notebook

## How to use
1. Download the notebook files
    -   Click the green button above, and click download ZIP (or open this link: https://github.com/Nickp1993/4DC10-student/archive/refs/heads/main.zip )
    -   Extract the `notebooks` folder from the ZIP-file.
        - E.g. to `C:\4DC10\notebooks`
2. Every time you want to start jupyter notebook: 
    -   Open the anaconda prompt (found in windows menu)
    -   In anaconda, set the path to that of your notebooks folder by entering `cd <path>` with `<path>` the path of your notebooks folder. If you are not using your default drive (`C:\`), use `cd /D <path>`.
        - E.g. `cd C:\4DC10\notebooks`, or `cd /D F:\4DC10\notebooks`
    -   Enter `jupyter notebook`
    -	Wait till a local server has started, your browser should open it automatically, if not, open this link: http://127.0.0.1:8888/ 
    -   Open one of the notebooks (files with an `.ipynb` extension)
    -	In the menubar, click kernel > change kernel >  Python (pychEnv)
3. You can now use this notebook!
    -   You can now click run to execute the cells of the notebook one-by-one (jupyter notebooks work top-down)
    -   Look here to find out how jupyter notebook works: https://realpython.com/jupyter-notebook-introduction/
