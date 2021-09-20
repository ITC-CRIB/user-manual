## Geospatial computing platform’s user manual

### Setup

* To display Jupyter Notebooks in the manual, the [nbsphinx](https://nbsphinx.readthedocs.io/en/0.8.7/index.html) package is used. This package requires [pandoc](https://pandoc.org/>) to be installed on the system. 

* This repository includes a [Git submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules). The submodule is the [training-resources]() folder. Important to note that when this repository is normally cloned with `git clone <url>`, the `training-resources` folder is not populated with files. To clone this project and populate the `training-resources` folder use git clone --recursive <url>. Furthermore, to pull the latest changes for the submodule run git submodule update --remote.

### Build

To build the documentation website run `make html` which will generate a *_build*   folder. The generated folder will contain a *html* folder that includes all the assets for hosting the documentation.
