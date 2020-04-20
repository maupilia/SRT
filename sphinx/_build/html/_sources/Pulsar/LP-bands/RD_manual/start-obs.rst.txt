.. SRT procedures documentation master file, created by
   sphinx-quickstart on Mon Aug  7 16:44:28 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


.. toctree::
   :maxdepth: 1


.. _start-PuRD:

Start the observations
======================

$ : commands to insert in a shell

> : commands to insert in the operatorInput panel

.. |logo| image:: monocle_.png
..    :width: 20pt
..    :height: 20pt
..   :align: left
|logo|: check the execution on the monitor



In the operatorInput panel
--------------------------


#. Insert your project number :

    ``> project=[projectID]``    |logo| :numref:`srt_scheduler`


#. Initial setup :

    ``> antennaReset``

    ``> setupPLP`` |logo| :numref:`srt_receivers_LLP`


#. Select the active surface shape (Parabolic for L and P-band observations) :

    ``> asSetup=P``  |logo| :numref:`srt_activesurface`


#. Choose the relevant LP-band filter, e.g.

    ``> receiversMode=L2L4`` |logo| :numref:`srt_receivers_LLP`


#. Insert the Local Oscillator value in MHz:

    ``$ setLO=...`` |logo| :numref:`srt_receivers_LLP`


#. Set the attenuations (to zero) for the 2 polarizations arriving at the Total Power backend (this may change depending on the settings of the new IF distributor).

    ``> setAttenuation=0,15`` |logo| :numref:`srt_genericBackend`

    ``> setAttenuation=1,15`` |logo| :numref:`srt_genericBackend`

    ``> setAttenuation=2,0`` |logo| :numref:`srt_genericBackend`

    ``> setAttenuation=3,0`` |logo| :numref:`srt_genericBackend`

#. Begin the schedule by indicating the start scan [N] or subscan [N_n] in the SCD file :

    ``> startSchedule=[projectID]/[schedulename].scd,[N_n]`` |logo| :numref:`srt_scheduler`

     If your schedule is LST-based (like for LEAP schedules), the antenna points to the relevant source as soon as you launch the schedule, even before the designated start time of observations (but you can start data acquisition with the ROACH1 at a later time). Check on the monitor each time that the antenna is pointing at and **TRACKING** the right source.



On the LEAP cluster (using VNC):
---------------------------------


#. In W1: type a command here to select baseband mode:

    ``$ ~/roach/scripts/baseband.sh``


Before starting data acquisition, do the following:

#. W1: initial setup in Control directory:

    ``$ ./control_init.sh``

This will ssh to all 8 nodes and start the daemons in another window (W2).

#. When the antenna is tracking the first source and you are ready to start data acquisition, go to W and type:

    ``$ ./start.csh``

     Data acquisition has now started with the ROACH1.

#. Immediately launch the control software (in W1) which obtains parameters from the antenna and automatically starts and stops observations, depending on whether the antenna is **TRACKING** or **SLEWING**:

    ``$ ./control.csh``

If necessary, this code can be interrupted (using Control-C) and re-started at any time while the antenna is tracking the same source, without any consequences.

You should now see: **“no change. keep doing what you’re doing”** while the antenna keeps tracking the same source. If all goes well, you won’t need to do anything else with data acquisition for the remainder of the session. You should however check the control window (W1) once in a while for possible errors (e.g. antenna WARNING).
