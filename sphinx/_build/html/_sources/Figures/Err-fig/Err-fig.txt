.. SRT procedures documentation master file, created by
   sphinx-quickstart on Mon Aug  7 16:44:28 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


Primary Control Panel ACU
=================

When the emergency stop button is pressed, different messages are in red,
as indicated in the following figure:

        .. _srt_ACU_redbutton:

        .. figure:: srt_ACU_redbutton.png
	   :align: center

          Situation of the ACU panel when the emergency button is pressed.


At the end of your observations, do not press the emergency stop button when
the **Stow Pin Motion** is yellow.

        .. _srt_ACU_stowpin:

    	.. figure:: srt_ACU_stowpin.png
	   :align: center


Wait until **Axis blocked** appears in red to press the emergency stop, as in the following figure:

        .. _srt_ACU_axisblocked:

    	.. figure:: srt_ACU_axisblocked.png
	   :align: center


AntennaBoss
========


Observatory
========


Mount
====

        .. _srt_mount:

    	.. figure:: srt_mount.png
	   :align: center


GenericBackend
==========


ReceiversBoss
==========


Scheduler
======

The antenna is not in tracking when the @ is red.
Note that it can also be red when the antenna is in slewing (to reach
the position of a target).

When the status of the scheduler is in FAILURE and the scan/subscan
number is frozen, stop the schedule.

        .. _srt_scheduler:

     	.. figure:: srt_scheduler.png
	   :align: center

           The scheduler status is in FAILURE !!!!!!!!.


MinorServo
=======




Logging Display
==========




Active Surface
=========






MeteoClient
========

The real-time monitoring of the wind velocity is performed with the
meteoClient on a nuraghe-mng shell: ``$ meteoClient``.
If the wind speed exceeds 60 km/h, the antenna must be stowed immediately.

        .. _srt_windspeed:

     	.. figure:: srt_windspeed.png
	   :align: center

           The wind speed exceeds 60 km/h, as indicated with the red horizontal line.
