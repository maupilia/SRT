.. SRT procedures documentation master file, created by
   sphinx-quickstart on Mon Aug  7 16:44:28 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

  
======================
End of the session
======================

.. toctree::
   :maxdepth:1


$  : commands to insert in a shell

>  : commands to insert in the operatorInput panel

.. |logo| image:: monocle_.png
..    :width: 20pt
..    :height: 20pt
..   :align: left
|logo|: check the execution on the monitor

======================

Your observations are now finished, we can stop the schedule and park
the antenna.


In LEAP VNC
------------------

1. W: Do a ``Control-C`` to end the ./control.csh script.

2. W: ``$ ./end.csh`` to end data acquisition and close the daemons.

3. In each node: ``$ sudo halt``

On nuraghe-mng
----------------

1. Stop your schedule :

    ``> stopSchedule``   *interruption of the current subscan* |logo| :numref:`srt_scheduler_end`

      or

    ``> haltSchedule``    *the schedule stops at the end of the on-going subscan.*




2. Park the minor servo, active surface and antenna

   ``> goTo=180d,89d`` |logo| :numref:`srt_mount_ok`

   ``> servoPark`` |logo| :numref:`srt_minorservo_end`

   ``> asPark`` |logo| :numref:`srt_activesurface`

   ``> antennaPark`` |logo| :numref:`srt_mount_antennareset`




Block the axes of the antenna
------------------------------

Look at the ACU monitor, wait until
**Axis blocked** appears in red. It can take a few minutes after the command
``> antennaPark`` has been given (:numref:`srt_ACU_axisblocked`).

Only at this moment, you can press on the emergency stop button
(:numref:`srt_ACU_redbutton`).

