
# PyCh

PyCh is a Python package based on SimPy for discrete-event simulation.
It is a tool developed for the course "Analysis of production systems" (4DC10).
PyCh is a port of [Chi3](https://cstweb.wtb.tue.nl/chi/trunk-r9682/).


## Contents
- Tutorials chapter 1 - 10 contain the tutorial on how to use PyCh
- Offline_PyCh_tutorial2022 contains the tutorial in PDF format (for reference)
- Assignment.ipynb contains the jupyter notebook for the course assignment
- LectureNotesExamples.ipynb - contains the jupyter notebook of all models used in the lecture notes
- LectureSlidesExamples.ipynb - contains the jupyter notebook of all models used in the lecture slides


## How to install
1.	Download and install the latest version of anaconda
    -	https://www.anaconda.com/products/individual
    -	Note that you can `Skip registration` if you don't want to provide your email address.

For Windows

2.	Open an `Anaconda prompt (Anaconda3)` (you can type it in the windows bar below), and enter the following commands:
    - `conda create --name pychEnv`
        - Enter `y` (for yes)
    -	`conda activate pychEnv`
    -	`conda install git pip ipykernel notebook`
        - Enter `y` (for yes)
    -	`python -m ipykernel install --user --name pychEnv --display-name "Python (pychEnv)"`
    -	`pip install git+https://github.com/Nickp1993/Pych/`
    -	Close this window (do not continue with the "how to use" without closing!)

For macOS

2.	Open a terminal and enter the following commands:
    - `conda create --name pychEnv`
        - Enter `y` (for yes)
    -	`conda activate pychEnv`
    -	`conda install git pip ipykernel notebook`
        - Enter `y` (for yes)
    -	`python3 -m ipykernel install --user --name pychEnv --display-name "Python (pychEnv)"`
    -	`pip install git+https://github.com/Nickp1993/Pych/`
    -	Close this terminal

For all OS

3. Clone the notebook files from your group's GitLab repository to your local machine. 
- If you have used GitKraken in the course 4TC400 Model-based systems engineering, you can immediately perform the steps as described [here](https://cstweb.wtb.tue.nl/4tc00/tooling/git/index-use.html#initiating-your-workspace-cloning) and locate your group's repository within the group `x4dc10/2024` (i.e., the repository for this course, not the one from 4TC400). 
- If you haven't done 4TC400 before, follow the instructions below under *GitKraken* for more information on installing GitKraken and cloning your repository.
- If you want to use another Git GUI or the command line, you can clone your repository by navigating to your group repository: `gitlab.tue.nl/x4dc10/2024/<group name>/<group name>-pych-student`, where `<group name>` is structured as `<group number>_<name student 1>_<name student 2>_<name student 3>`, for example `045_adan_goorden_reniers`; click the blue `Code` button above, and copy the address under `Clone with HTTPS`; and then clone the repository to your local machine using your favorite Git tool.

4.	You have finished installation, continue with the "How to use" below to start a notebook


## How to use
1. Get work from your teammates on your local system using Git `pull`.
2. Every time you want to start jupyter notebook:
    -   (Windows) Open the anaconda prompt (found in windows menu) and enter `conda activate pychEnv`
    -	(macOS) Open a terminal and enter `conda activate pychEnv`
    -   Check that the bottom line starts with `(pychEnv)` 
    -   In anaconda/terminal, set the path to that of your notebooks folder by entering `cd <path>` with `<path>` the path of your notebooks folder. If you are not using your default drive (`C:\`), use `cd /D <path>`.
        - E.g. `cd C:\4DC10\notebooks`, or `cd /D F:\4DC10\notebooks`, or `cd Users/goorden/courses/4dc10/notebooks`
    -   Enter `jupyter notebook`
    -	Wait till a local server has started, your browser should open it automatically, if not, [try clicking this links](http://127.0.0.1:8888/)
    -   Open one of the notebooks (files with an `.ipynb` extension). Note that you can open multiple notebooks from this overview
    -	In the menubar, click kernel > change kernel >  Python (pychEnv)
3. You can now use this notebook!
    -   You can now click run to execute the cells of the notebook one-by-one (jupyter notebooks work top-down)
    -   [Click this link for information on how jupyter notebook works](https://realpython.com/jupyter-notebook-introduction/)
4. Save, commit, and share your work with your teammates, which can be done at any point in time, i.e., no need to close the jupyter notebook server for this
    -   Jupyter notebooks should be saved automatically, but you can always save them manuall (just to be sure)
    -   Make a `commit` of your changes using GitKraken (See [here](https://learn.gitkraken.com/courses/git-foundations) if you need a reminder on how to do this)
    -   `Push` the commit to the TU/e GitLab server so your contributions become available to your teammates
5. When done, you can close the jupyter notebook server in the terminal by pressing `ctrl+c` (the nice way) or simply closing the terminal/anaconda window (the easy way).


## GitKraken
Proper version control is important when collaborating on files. Nowadays, cloud-based office products like Microsoft Office 365 and Google Docs/Sheets/Slides arrange this behind the scenes for word documents, sheets and presentation files. For other files, like models or software, we need to arrange version control ourselves. One popular version control system is Git. 

1. Please familiarize yourself with the basics of Git using [these instructions](https://cstweb.wtb.tue.nl/4tc00/tooling/git/index-intro.html) or this 4-min [YouTube video](https://youtu.be/e9lnsKot_SQ?si=ReV_tLW6T7e1r5PB).

Git can be used through a command line, but there exists numerous graphical user interfaces to use Git. A very intuitive and easy-to-use GUI is GitKraken. This is a paid tool, but free for students with a GitHub Student Developer Pack. 

2. If you haven't used GitKrake before, follow [these instructions](https://cstweb.wtb.tue.nl/4tc00/tooling/git/index-use.html) to setup GitKraken.

3. The course specific workflows in GitKraken from [here](https://cstweb.wtb.tue.nl/4tc00/tooling/git/index-use.html#course-specific-workflows-in-gitkraken) also apply in this course. 

4. There are plenty of materials online on learning Git. Some good written material is highlighted [here](https://cstweb.wtb.tue.nl/4tc00/tooling/git/index-use.html#further-reading), but you can also find a lot of videos on YouTube. 


## Troubleshooting
- Most errors are caused by not following the *How to install* instruction carefully enough.
- If you get the error `No module named 'PyCh'` when you try to run the command `from PyCh import *`, then PyCh has likely not been installed correctly (try installing again) *or* you are not running the jupyter notebook from the `pychEnv` virtual environment (use `conda activate pychEnv` before starting jupyter).
- The same goes if you get a `Numpy importerror`.
- Make sure you open ``Anaconda Prompt (Anaconda3)`` and not another version (such as `Anaconda Prompt` **without Anaconda3**)!
- If you get a `EnvironmentNotWritableError` or `Error [WinError 2]` during installation, try running the anaconda prompt as administrator, and then try installing again.
- If you get a `OpenSSL` or `CondaSSLError`, the solution is as follows:
    1. Find your anaconda installation directory (e.g. `C:\ProgramData\Anaconda3` or `C:\Users\<username>\Anaconda3`)
    2. Go to the subdirectory`\Anaconda3\Library\bin\` and copy the files `libcrypto-1_1-x64.dll` and `libssl-1_1-x64.dll`.
    3. Paste these files in the following subdirectory: `\Anaconda3\DLLs\`.
- If you get an error code 128 while executing `pip install git+https://github.com/Nickp1993/Pych/`, you can instead try the following command: `pip install https://github.com/Nickp1993/PyCh/archive/master.tar.gz`.
- If you had a previous installation of Anaconda, this could cause issues. If so, contact a TA for help. The easiest solution generally is a clean install of Anaconda.
- WINError 225: Temporarily disable your antivirus while performing the installation.
