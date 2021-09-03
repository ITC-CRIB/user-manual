Platform
=========

This page contains information about the platform itself. For example, how to access it, its limitations and the underlying hardware, etc.

Access the platform
-------------------

You can access to the platform at https://crib.utwente.nl/geospatialhub/ by using your personal University of Twente account (i.e., e-mail address and password).

Unless stated otherwise, all additional services (e.g. GeoServer, Gitea) can also be accessed in the same way. Each service may require you to sign in separately.


Use the platform
----------------

The default interface of the platform is `JupyterLab <https://jupyter.org/>`_, which enables you to work with interactive notebooks and documents through text and code editors, terminals, and other custom components (e.g. map widgets).

If you are new to JupyterLab (or Jupyter notebooks in general), a good starting point is its `official documentation <https://jupyterlab.readthedocs.io/en/stable/index.html>`_, which includes a detailed user guide. There is also a nice and short (~ 6 min.) `introduction video <https://www.youtube.com/watch?v=A5YyoCKxEOU>`_ available.

For specific components integrated to the platform (e.g. `Code Server <https://github.com/cdr/code-server>`_), please refer to their own documentation.


Platform security
-----------------

Your connection to the platform is secure (i.e. encrypted) and has **A rating** from `SSL Labs <https://www.ssllabs.com/>`_.

Your working environment is created on demand and isolated from the others which are active on the platform. Therefore, your assets (e.g. files, documents, images, etc.) are only accessible to you.

The platform uses University of Twente `LDAP <https://en.wikipedia.org/wiki/Lightweight_Directory_Access_Protocol>`_ service to authenticate your credentials also through a secure connection and does not store your password.


Run multiple platform instances at the same time
------------------------------------------------

A dedicated container is spawned for you when you first login. When you login again while you are logged in (e.g. from another browser window or another machine) you connect to the same container. Therefore, it is not possible to have two different platform instances concurrently.

Please `contact us <https://crib.utwente.nl/support/open.php>`_ if you need more instances, e.g. to finish your thesis study. We can create an external account for you which will allow you to use a second instance.

.. tip::
    Profile your code to understand resource usage and bottlenecks. This may help you to use your instance efficiently.

.. tip::
    Consider using a distributed computing framework (e.g. `Dask <https://dask.org/>`_) to improve the computing performance.


Run long duration tasks
-----------------------

Running long duration tasks is possbile. The users, who use the platform for deep learning purposes, usually have tasks that last *several days.* However, you should be connected to the platform during the computation period, i.e. your web browser should be open all the time.

.. tip:: 
    If you cannot ensure connection from your own computer, connect to a UT computer by remote desktop and use that computer to connect to the platform.

.. warning:: 
    For long-duration tasks do not trust service availability and implement precautionary measures (e.g. checkpoints).


Disconnect from the platform for a short period while keeping running tasks alive
---------------------------------------------------------------------------------

If you log out from the platform ``(File > Log out)``, your container is terminated. Hence, all running tasks are also terminated. But if you simply **close the browser window**, the platform keeps your container and all active tasks running for *one hour*. If you re-connect within this one-hour period, you connect to the same container.

.. tip::
    Use a file-based output mechanism (i.e. logging) to backup standard output whenever possible.

.. warning::
    When you close the browser window, running tasks lose their output streams. Therefore, although they continue to run, you won't see their output after re-connecting to the same container.


Edit a notebook collaboratively in real time
--------------------------------------------

Starting with `JupyterLab 3.1 <https://jupyterlab.readthedocs.io/en/stable/getting_started/changelog.html#id26>`_, file documents and notebooks `support collaborative editing <https://jupyterlab.readthedocs.io/en/stable/user/rtc.html>`_ and this feature is enabled on the platform.

The collaborative editing feature enables collaboration in real-time between multiple clients **without user roles**. If you share the URL of a document to other users, they will have access to **the same environment you are working on** and they can write and execute cells. Moreover, you can **see the cursors from other users** with an anonymous username.

This feature is quite new and currently requires some manual steps, which are listed below:

1. `Log in <https://crib.utwente.nl/geospatialhub/>`_ to the platform.
2. On computing unit selection page, click Token link at the top menu.
3. Click ``Request new API Token`` button.
4. Copy the API token provided and paste it somewhere temporarily (e.g. Notepad).
5. Click Home link at the top menu.
6. Select a computing unit.
7. Locate the notebook you want to edit collaboratively in the file browser sidebar.
8. Right click on the file and select ``Copy Sharable Link`` menu.
9. Paste the link where you pasted API token previously and modify it by adding the token as a URI parameter. Example:

API Token:
**9f77c98cf27e492f40b8fc15dfcaccfa**

Link: **https://crib.utwente.nl/geospatialhub/user/jovyan/doc/tree/example.ipynb**

Modified link: **https://crib.utwente.nl/geospatialhub/user/jovyan/doc/tree/example.ipynb?token=9f77c98cf27e492f40b8fc15dfcaccfa**

10.  Share the modified link with your collaborators.

.. warning::
    The API token allows other users to access not only the document you selected, but your account in general. Therefore, they can access all other documents, including your private files. Be careful while using this feature.


Delete a non-empty folder
-------------------------

This guide applies to situations when a non-empty folder has to be deleted from the system. Since this
functionality is not natively supported in JupyterLab yet, it can be done in one of two ways, either using
remote desktop or the terminal. Here, we provide step-by-step instructions on how to do this both ways.

.. warning::
    Deleted files cannot be recovered. Please be careful while deleting files and folders.


Using remote desktop
^^^^^^^^^^^^^^^^^^^^

1. Open remote desktop application

To open remote desktop, firstly, click on ``Application`` which is located in the top tool bar,
and then select ``Remote Desktop``. You should be presented with a desktop view.

2. Locate your folder and delete it

To open the file manager, double click on the ``Home`` folder you see on the desktop. From there
on navigate to the folder you wish to delete. Right click on the folder and select ``Delete``.


Using the terminal
^^^^^^^^^^^^^^^^^^

1. Open the terminal

To open the terminal, firstly, click on ``File`` which is located in the top tool bar, then hover
over ``New`` and finally select ``Terminal``. Now, you should be able to see the terminal.

2. Locate your folder

To interact with the terminal you must write commands. Firstly, to see the files and folders in
the folder you are currently in, write the command ``ls``. Then, to
move to one of the folders you see on the screen after ``ls`` command, use the command ``cd folder``
replacing *folder* with the name of the folder you want to move to. If you want to move backwards
from a folder, use the command ``cd ..``. Using the two aforementioned commands, navigate to the folder
that contains the folder you wish to delete.

3. Delete the folder

Before you delete your folder, use the ``ls`` command to make sure you see your folder listed there.
Then, use the command ``rm -rf folder`` replacing *folder* with the name of your folder.


Jupyterlab extensions
---------------------

Available extensions
^^^^^^^^^^^^^^^^^^^^

The list of all available Jupyterlab extensions is available :doc:`here </pages/jupyterlab-extensions>`.

Unavailable extensions
^^^^^^^^^^^^^^^^^^^^^^

.. csv-table:: 
        :header: "Extension", "Description", "Version", "Reason", "Alternative"
        :widths: 10, 10, 10, 10 ,10
     
        "jupyterlab_nvdashboard", "A JupyterLab extension for displaying GPU usage dashboards", 0.6.0, "Requires NVML (not supported)"
        "jupyterlab-hdf5", "A Jupyter Notebook server extension that provides APIs for fetching hdf5 contents and data",	0.6.0,	"Does not support JupyterLab 3.x"
        "jupyterlab-system-monitor", "Extension to display system metrics",	0.6.0, "Disabled due to performance issues", "Terminal > top"
        "jupyterlab-topbar-extension", "Generic extension to expose the top bar area", 0.5.0, "Disabled due to performance issues",	"Terminal > top"


Nodes on the platform
---------------------

The list of all available platform computing nodes is available :doc:`here </pages/nodes>`.
