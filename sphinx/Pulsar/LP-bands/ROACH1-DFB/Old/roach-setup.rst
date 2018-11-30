.. SRT procedures documentation master file, created by
   sphinx-quickstart on Mon Aug  7 16:44:28 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


.. toctree::
   :maxdepth: 1
  
======================
Roach setup
======================

Initial setup for the LEAP cluster.


In the VNC
----------

#. Open a terminal window and go to :

    ``$ ~/externalClient/Control/``

     This window will be used to start and stop data acquisition.

#. Open another tab and select P-band:

      ``$ ~/roach/scripts/setPband.sh``
      
      This code changes the IP table so that we are selecting the desired 8 sub-bands.


#. Select baseband mode:

    ``$ ~/roach/scripts/baseband.sh``


