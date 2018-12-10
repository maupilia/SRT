.. SRT procedures documentation master file, created by
   sphinx-quickstart on Mon Aug  7 16:44:28 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


.. toctree::
   :maxdepth: 1

.. _bef-PuMPRO:


Before observing
====================

After the standard checks:

1. On a desktop open the leap0 VNC session using
**VNCViewer** or **TigerVNC** and selecting **leap0:1**  *(ask for
password)*.

If it is not active:

2. Log on to the LEAP cluster :

    ``$ ssh -X user@leap0``     *ask for password*


3. Launch a VNC session once logged on to leap0 :

    ``leap0: $ vncserver &``



On the LEAP cluster (using VNC):
---------------------------------

Initial setup for the LEAP cluster:


#. Open a window (W1) and go to :

    ``$ ~/externalClient/Control/``

     This window will be used to start and stop data acquisition.

#. In W1: type a command to select P-band (and not L-band):

    ``$ ~/roach/scripts/setPband.sh``
