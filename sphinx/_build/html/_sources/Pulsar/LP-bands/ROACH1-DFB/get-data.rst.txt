.. SRT procedures documentation master file, created by
   sphinx-quickstart on Mon Aug  7 16:44:28 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


.. toctree::
   :maxdepth: 1

.. _get-PuRD:

Getting your data
=================


Your DFB data are in your ProjectID directory on discos-console.

You can download them on your computer whenever you want during the
observations.

   ``$ scp -r  projectID@discos-console:data/yyyymmdd .``


The ROACH1 data have been written on the nodes of the LEAP cluster. After the observation run, this baseband data needs to be de-dispersed and folded (it may take a few hours and no other observations with the ROACH1 can take place while the cluster is being used).
The folding or search procedure you have required in your proposal will be performed offline by your project friend.

The final archive data will be stored on the head node of the LEAP cluster (leap0) in ~/DATA/.

This data (in .ar format) can then be transferred to nuraghe-mng or a
personal computer using "scp". In LEAP cluster VNC:

     ``$ scp -r ~/DATA/[today’s date]  [projectID]@nuraghe-mng:/archive/data/[projectID]/``
