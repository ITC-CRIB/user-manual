.. include:: .special.rst

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

Yes, you can. The users, who use the platform for deep learning purposes, usually have tasks that last *several days.* However, you should be connected to the platform during the computation period, i.e. your web browser should be open all the time.

.. tip:: 
    If you cannot ensure connection from your own computer, connect to a UT computer by remote desktop and use that computer to connect to the platform.

.. warning:: 
    For long-duration tasks do not trust service availability and implement precautionary measures (e.g. checkpoints).

Please `contact us <https://crib.utwente.nl/support/open.php>`_ for specific needs.


Disconnect from the platform for a short period while keeping running tasks alive
---------------------------------------------------------------------------------

If you log out from the platform ``(File > Log out)``, your container is terminated. Hence, all running tasks are also terminated. But if you simply **close the browser window**, the platform keeps your container and all active tasks running for *one hour*. If you re-connect within this one-hour period, you connect to the same container.

.. warning::
    When you close the browser window, running tasks lose their output streams. Therefore, although they continue to run, you won't see their output after re-connecting to the same container.

.. tip::
    Use a file-based output mechanism (i.e. logging) to backup standard output whenever possible.


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
