# Work in progress

## To-do List

- GeoServer LDAP integration
- Dataverse LDAP integration
- Check high memory allocation issue with CUDA/CuPy
  - The reason is identified: pre-allocation of GPU memory to speed-up processing.
  - Unfortunately this doesn't work nicely with unified CPU-GPU memory architecture
  - Framework specific solutions exists and will be implemented.
- Spark usage example

## Waiting List

- **Application**: [Paraview](https://www.paraview.org) - 3D data analysis and visualization application
- **Framework**: [Geonode](https://geonode.org/) - Open Source Geospatial Content Management System
- **Application**: [QGIS Server](https://www.qgis.org) - WMS, WFS and WCS implementation that implements advanced cartographic features for thematic mapping
- **Application**: [Spyder](https://www.spyder-ide.org/) - Scientific Python development environment

## Finished

- ODC installation
- **Application**: [ODK](https://opendatakit.org/) - Open Data Kit
- **Application** : [SNAP](http://step.esa.int/main/download/snap-download/) - SNAP and the Sentinel Toolboxes
- **Application**: [Firefox](https://www.mozilla.org/en-US/firefox/) - Safe and easy web browser from Mozilla
- **Application**: [PyCharm](https://www.jetbrains.com/pycharm/) - Python Integrated Development Environment (IDE)
- **Application**: [FragStats](https://www.umass.edu/landeco/research/fragstats/fragstats.html) - calculates landscape metrics (can be installed through Wine)
- **Application**: [GMTSAR](https://topex.ucsd.edu/gmtsar/) - InSAR processing system based on GMT
- **Application**: [Glueviz](https://glueviz.org/) - Multi-dimensional linked-data exploration
- **Framework**: [Horovod](https://horovod.ai/) - Framework for distributed deep learning training using TensorFlow, Keras, PyTorch, and Apache MXNet.
- **Framework**: [TensorFlow Addons](https://github.com/tensorflow/addons) - Useful extra functionality for TensorFlow 2.x maintained by SIG-addons 
- **Framework**: [fast.ai](https://www.fast.ai/) - Making neural nets uncool again
- **Framework**: [SpaCy](https://spacy.io/) - Industrial-strength NLP
- **Language**: [Rust](https://www.rust-lang.org) - Fast and memory-efficient programming language
- **Application**: [NetLogo](https://ccl.northwestern.edu/netlogo) - Multi-agent programmable modeling environment
- **Application**: [GRASS](https://grass.osgeo.org/) - Geographic Resources Analysis Support System
- **Framework**: [MLflow](https://mlflow.org/) - Open source platform for the machine learning lifecycle
- **System Upgrade**: Python 3.6 -> Python 3.8
  - Python 3.6 currently receives only security updates and has end-of-life of 2021/12.
  - NVIDIA L4T is based on Ubuntu 18.04, which has Python 3.6. Some packages are only available for Python 3.6 (e.g. tensorrt)
  - Alternative Docker files for Ubuntu 20.04 + Python 3.8 are in production.
  - All packages are migrated, except the following heavy ones:
    - *TensorFlow*: Build commands ready, to be tested.
    - *MXNet*: Build commands ready, to be tested.
    - *ONNX Runtime*: Build commands ready, to be tested.
    - *Keras*: Pending TensorFlow
- **Bug Fix**: JAX CPU-backend
  - This was a difficult bug to identify, but it is fixed now (https://github.com/google/jax/issues/5679)
  - Will be available with Python 3.8
- **Application**: [Orange3](https://orangedatamining.com/) - Interactive data analysis
  - Built and tested, ready to deploy.
- **Application**: [RStudio](https://rstudio.com/) - Integrated development environment for R
  - Built, but QT GLX fails at runtime.
   - It looks like we need to change VNC server again, possibly to [TurboVNC](https://www.turbovnc.org/)
  - Tried TurboVNC, but solution also works with TigerVNC.
- PostgreSQL LDAP integration