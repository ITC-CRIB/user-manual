Unsupported extensions
======================

.. csv-table:: 
        :header: "Extension", "Description", "Version", "Reason", "Alternative"
        :widths: 10, 10, 10, 10 ,10
     
        "jupyterlab_nvdashboard", "A JupyterLab extension for displaying GPU usage dashboards", 0.6.0, "Requires NVML (not supported)"
        "jupyterlab-hdf5", "A Jupyter Notebook server extension that provides APIs for fetching hdf5 contents and data",	0.6.0,	"Does not support JupyterLab 3.x"
        "jupyterlab-system-monitor", "Extension to display system metrics",	0.6.0, "Disabled due to performance issues", "Terminal > top"
        "jupyterlab-topbar-extension", "Generic extension to expose the top bar area", 0.5.0, "Disabled due to performance issues",	"Terminal > top"