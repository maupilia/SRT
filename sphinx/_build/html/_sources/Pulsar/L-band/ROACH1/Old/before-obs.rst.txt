.. SRT procedures documentation master file, created by
   sphinx-quickstart on Mon Aug  7 16:44:28 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

  
**Notes :** The following instructions are for observing at L-band with the ROACH1 in baseband mode. The observed bandwidth is limited to 128 MHz and corresponds to 1332-1460 MHz (the LEAP band). This mode is adequate for LEAP observations or for generic L-band observations in baseband mode, with a limited 128 MHz bandwidth.
                

======================
Before observing
======================

.. toctree::
   :maxdepth: 1

After the standard checks:

1. On the MISC desktop of nuraghe-mng open the leap0 VNC session using
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


#. Open a window (W) and go to :

    ``$ ~/externalClient/Control/``

     This window will be used to start and stop data acquisition.

#. In W: type a command here to select L-band (and not P-band):

    ``$ ~/roach/scripts/setLband.sh``




