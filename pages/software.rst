Software applications/packages
==============================

This page contains information about software applications and software packages on the platform. This includes what software is
and isn't available, how to install your own software, etc. 

Supported software packages
----------------------------------------

.. toctree::
   :maxdepth: 3

   python/index
   r-packages
   system-packages/index
   jupyterlab-extensions/index
   custom-built


Why xxx is not available?
-------------------------

We are trying to make widely-used software packages and libraries available with a special focus on geo-information and earth observation. In fact, we did a survey to understand your needs and determined the list accordingly. We will periodically review this list and add more packages.

If the software package you need is not available on the platform (yet), the reasons could be:

* We may not be aware of it. Just `contact us <https://crib.utwente.nl/support/open.php>`_ and tell us what you need. Most probably we can make it available quickly, especially if it is an open source software.

* It might be a package we are currently working on. Some packages have a long list of dependencies and they are difficult to setup, especially on a platform composed of special units (i.e. `Jetson AGX Xavier <https://www.nvidia.com/en-us/autonomous-machines/embedded-systems/jetson-agx-xavier/>`_) which are quite different from standard equipment (e.g. servers). Probably we solve all the issues and make it available soon.

* It might be a package that is not supported by the platform architecture (`Linux <https://en.wikipedia.org/wiki/Ubuntu>`_ / `ARM v8.2a <https://en.wikipedia.org/wiki/Project_Denver>`_). But there might be some alternatives available and we can help you to find them if you `contact us <https://crib.utwente.nl/support/open.php>`_.

* It might be proprietary requiring a license. Currently we don't support such software packages, but this may change in the future. Please `let us know <https://crib.utwente.nl/support/open.php>`_ if you need such software products.


Why the latest version of xxx is not available?
-----------------------------------------------

We do our best to make the latest versions of software packages and libraries available. However, occasionally certain versions of the packages are not compatible to each 
other or not fully supported by the platform architecture (`Linux <https://en.wikipedia.org/wiki/Ubuntu>`_ / `ARM v8.2a <https://en.wikipedia.org/wiki/Project_Denver>`_) - so we have to choose. If you are not happy with the selection please `let us know <https://crib.utwente.nl/support/open.php>`_.


Install R, Python, Julia, etc. packages
---------------------------------------

For Python, open a terminal and enter the command:

``pip install or pip install ==``

For R, enter the command in an interactive R notebook:

``install.packages('', repos='')``

For other languages, please refer to the user documentation or `contact us <https://crib.utwente.nl/support/open.php>`_.

Packages are installed to your home directory (i.e. /home/jovyan). Therefore, they are permanent. But they are not updated automatically and you should keep them up to date.

`Conda <https://docs.conda.io/en/latest/>`_ is not supported, but you can use `virtual environments <https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/>`_, if necessary.

.. note::
        You may encounter installation errors if the package requires additional system libraries or it is not compatible with the architecture of the computing unit. Please `contact us <https://crib.utwente.nl/support/open.php>`_ if you encounter any difficulties. We can install it for you, which will make it also available to other users.

.. warning::
        Local package dependencies are not guaranteed after platform updates.

.. warning::
        Local packages might be architecture dependent.


Install additional software applications
----------------------------------------

System-wide software packages are protected and you **cannot** install software that needs to be installed to the system directories (e.g. /usr or /usr/local). But you can install software packages and portable applications to your workspace (i.e. home, private, or shared folders). Please `contact us <https://crib.utwente.nl/support/open.php>`_ if you encounter any difficulties.

.. note::
        You cannot install software by using the default package manager of Ubuntu (apt)

.. note::
        Custom software are not updated automatically. You should keep them up to date.

.. warning::
        Custom software might be architecture dependent (e.g. arm64/aarch64 for NVIDIA Jetson AGX, amd64/x86_64 for PowerEdge). If you install a software for one architecture, it may not work with the other one.


Install Windows applications
----------------------------

Windows applications are supported through emulation by `Wine <https://www.winehq.org/>`_. They are not supported on NVIDIA Jetson AGX units, so you need to use a computing unit with Intel architecture (e.g. PowerEdge units). Because they run through emulation, Windows applications are not guaranteed to work 100%. 

For Win32 applications, open a terminal and enter the command:

``WINEPREFIX="$HOME/.wine32" wine``

For Win64 applications, open a terminal and enter the command:

``WINEPREFIX="$HOME/.wine64" wine``

C Drive is located at $HOME/.wine/drive_c

Please `contact us <https://crib.utwente.nl/support/open.php>`_ if you encounter any difficulties.


Use MATLAB
------------

MATLAB (R2021a), Simulink, and selected toolboxes are available on the platform to the UT employees and students through the campus-wide license. Please follow the following steps to use MATLAB and related products:

1. `Log <https://crib.utwente.nl/geospatialhub/>`_ in to the platform.
2. Select a computing unit with **Intel** architecture (e.g. PowerEdge, Optiflex). *MATLAB is currently not supported on Jetson units.*
3. Open remote desktop connection selecting ``Remote Desktop (NoVNC)`` icon from the launcher menu.
4. On the remote desktop, select ``Applications > Research > MATLAB`` from to top menu
5. Enter your **e-mail address linked to your MathWorks account** and click ``Next``. Normally this should be your UT e-mail address, but it should be activated first. You can find more information at the `UT Service Portal <https://www.utwente.nl/en/service-portal/hardware-software-network/software/matlab-simulink>`_.
6. Enter your **MathWorks account password** and click ``Sign In``.

.. raw:: html

    <details>
        <summary>Expand to see the add-ons that are available with MATLAB</summary>
        </br>

.. csv-table:: 
        :header: "Add-on", "Version"
        :widths: 30, 10
     
        "Computer Vision Toolbox", 10.0
        "Curve Fitting Toolbox", 3.5.13
        "Database Toolbox", 10.1
        "Datafeed Toolbox", 6.0
        "Deep Learning Toolbox", 14.2
        "Financial Toolbox", 6.1
        "Global Optimization Toolbox", 4.5
        "Image Processing Toolbox", 11.3
        "Lidar Toolbox", 1.1
        "Mapping Toolbox", 5.1
        "Optimization Toolbox", 9.1
        "Parallel Computing Toolbox", 7.4
        "Partial Differential Equation Toolbox", 3.6
        "Reinforcement Learning Toolbox", 2.0
        "Risk Management Toolbox", 1.9
        "Signal Processing Toolbox", 8.6
        "Simulink", 10.3
        "Statistics and Machine Learning Toolbox", 12.1
        "Symbolic Math Toolbox", 8.7
        "Text Analytics Toolbox", 1.7
        "UAV Toolbox", 1.1
        "Wavelet Toolbox", 5.6

.. raw:: html

    </details>
    </br>


Use Dask 
--------

.. toctree::
   :maxdepth: 3

   how-to-dask.ipynb


Use HDFS service
----------------

.. toctree::
   :maxdepth: 3

   how-to-hdfs.ipynb


Install JupyterLab on Windows
-----------------------------

This guide shows step-by-step instructions on how to install JupyterLab on your own Windows computer. 

.. toctree::
   :maxdepth: 3

   jupyterlab-install-guide/index



Supported programming languages
-------------------------------

This is a list of all the programming languages supported on the platform through either command line or 
as interactive notebooks.

.. csv-table:: 
        :header: "Language", "Version"
        :widths: 20, 10
     
        "`Python <https://www.python.org/>`_", 3.8.5  
        "`R <https://www.r-project.org/>`_", 4.1.0
        "`Go <https://golang.org/>`_", 1.16.3
        "`Julia <https://julialang.org/>`_", 1.5.4
        "`Java <https://www.java.com/en/>`_", 11.0.11
        "`Scala <https://www.scala-lang.org/>`_", 2.12.12
        "`PHP <https://www.php.net/>`_", 7.4.3
        "`Ruby <https://www.ruby-lang.org/en/>`_", 2.7.0
        "`Octave <https://www.gnu.org/software/octave/index>`_", 6.2.0
        "`dot <https://graphviz.org/doc/info/lang.html>`_", 2.43.0
        "`gnuplot <http://www.gnuplot.info/>`_", 5.2
        "`*C <https://gcc.gnu.org/>`_", "GNU 9.3"
        "`*C++ <https://gcc.gnu.org/>`_", "GNU 9.3" 
        "`*Fortran <https://gcc.gnu.org/fortran/>`_", "GNU 9.3"
        "`*Perl <https://www.perl.org/>`_", 5.30
        "`*CUDA <https://en.wikipedia.org/wiki/CUDA>`_", 10.2


\*: Only available through the command line.