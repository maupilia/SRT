.. SRT procedures documentation master file, created by
   sphinx-quickstart on Mon Aug  7 16:44:28 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


.. toctree::
   :maxdepth: 1

.. _stop-PuRD:

End of the session
======================

>  : commands to insert in the operatorInput panel

.. |logo| image:: monocle_.png
..    :width: 20pt
..    :height: 20pt
..   :align: left
|logo|: check the execution on the monitor

Your observations are now finished, we can stop the schedule and park
the antenna.

On their respective desktops
----------------------------

#. Close the vnc session on seadas

#. Close the vnc session on psrdfb

#. Close the vnc session on leap0


On mng-dev
------------

#. Park the minor servo, active surface and antenna

   ``> goTo=180d,89d`` |logo| :numref:`srt_mount`

   ``> servoPark`` |logo| :numref:`srt_minorservo_end`

   ``> asPark`` |logo| :numref:`srt_as_park`

   ``> antennaPark`` |logo| :numref:`srt_mount_antennareset`  |logo| :numref:`srt_ACU_stowpin`




Block the axes of the antenna
------------------------------

Look at the ACU monitor, wait until
**Axis blocked** appears in red. It can take a few minutes after the command
``> antennaPark`` has been given (:numref:`srt_ACU_axis_blocked`).

Only at this moment, you can press on the emergency stop button
(:numref:`srt_ACU_redbutton`).
