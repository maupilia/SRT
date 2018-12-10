.. SRT procedures documentation master file, created by
   sphinx-quickstart on Mon Aug  7 16:44:28 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


.. toctree::
   :maxdepth: 1

.. _get-data:

Getting your data
==================

Your data are on discos-console.

You can download them on your computer whenever you want during the
observations.

   ``$ scp -r  [projectID]@discos-console:/home/[projectID]/data/yyyymmdd .``

or, if they are acquired with SARDARA:

   ``$ scp -r  [projectID]@discos-console:/home/[projectID]/sardaraData/yyyymmdd .``

.. Ask for the password.

..   $ scp -r  [projectID]@nuraghe-obs2:/archive/data/[projectID]/* .``

..   $ scp -r  gavino@nuraghe-mng:/archive/data/Maintenance/yyyymmdd .``
