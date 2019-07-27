# DOCKER
Docker repo for installation of python and jupyter in the container

### Install Docker
Go to the Docker website:  https://www.docker.com/products/docker-desktop and click on Download Desktop for Mac and Windows.  Follow the on-screen installation prompts to install.
**Note:**  Windows Users must enable hyper-V in both the bios and registry.

### Setup
- Download the *DOCKERFILE* and the *requirements.txt* file from the repo (jupyter-notebook branch)
- Browse through the *requirements.txt* file to see if anymore modules need to be added
- The current listing of modules is:
    - pandas
    - numpy
    - optlang
    - pulp
    - scikit-learn
    - leaflet
    - tensorflow
    - scipy
    - matplotlib
    - seaborn
    - statsmodels
    - plotly
    - flask
    - uuid
    - spacy
    - nltk
    - pysolr
    - sunburnt
    - networkx
    - swiglpk
    - xlrd
    - jupyter
These are some pretty standard data science modules but feel free to download or fork and your own modules
### Build and Run the Docker container
- Open Windows Powershell or Mac Terminal
- Navigate to directory where you put both the *DOCKERFILE* and the *requirements.txt* file, have to be in the same directory
- **Run:**  `docker build --tag=notebook .`
    - **Note:**  the period is important after *notebook* and must be included
- **Run:**  `docker run -p 8888:8888 -v <local-directory>:/notebooks notebook`
    - **Note:**  `<local-directory>` is the directory where you want the jupyter notebook to start in the file structure; Windows Users should also make sure that Docker has shared access to the drives on your computer, and use `C:/path/to/folder/` syntax instead of `\`.  Mac Users can just use their normal directory and path syntax.

### Opening the Notebook
In the terminal or Powershell window you will see something that says `copy url and paste into browser`, copy and past that URL with tokenid into your browser of choice!

Hope this helps!
