.. SRT procedures documentation master file, created by
   sphinx-quickstart on Mon Aug  7 16:44:28 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


Primary Control Panel ACU
=========================

At the end of your observations, do not press the emergency stop button when
the **Stow Pin Motion** is yellow as below.

        .. _srt_ACU_stowpin:

    	.. figure:: srt_ACU_stowpin.png
	   :align: center

           ACU panel after ``> antennaPark``.


Wait until **Axis blocked** appears in red before pressing the emergency stop, as in the following figure:

        .. _srt_ACU_axis_blocked:

    	.. figure:: srt_ACU_axis_blocked.png
	   :align: center

           ACU panel when the antenna is correctly parked.


When the emergency stop button is pressed, different messages are in red,
as indicated in the following figure:

        .. _srt_ACU_redbutton:

        .. figure:: srt_ACU_redbutton.png
	   :align: center

           ACU panel when the emergency button is pressed.




AntennaBoss
============


Observatory
============


Mount
======




GenericBackend
==============


ReceiversBoss
=============


Scheduler
==========

The antenna is not in tracking when the @ is red.
Note that it can also be red when the antenna is in slewing (to reach
the position of a target).

When the status of the scheduler is in FAILURE and the scan/subscan
number is frozen, stop the schedule.

        .. _srt_scheduler_failure:

     	.. figure:: srt_scheduler_failure.png
	   :align: center

           The scheduler status is in FAILURE


MinorServo
===========




Logging Display
===============

        .. _jlog-err:

     	.. figure:: jlog-err.png
	   :align: center

           The error messages are show in the Logging Display with a short explanation of the related problem.


        .. _log_emergency_stop:

    	.. figure:: log_emergency_stop.png
	   :align: center

           The warning message indicated by the blue arrow automatically appears when the emergency stop button is pressed.
	   
	   
Active Surface
===============

The active surface does not work properly if a large fraction (a whole sector) becomes red. It is a problem in K-band observations.

        .. _srt_AS-fraction-red:

     	.. figure:: AS-fraction-red.png
	   :align: center

           A fraction of the active surface (red squares) does not work properly.



MeteoClient
===========

The real-time monitoring of the wind velocity is performed with the
meteoClient on a nuraghe-mng shell: ``$ meteoClient``. The red
horizontal line corresponds to 60 km/h, the limit for observing with
SRT.

        .. _srt_windspeed:

     	.. figure:: srt_windspeed.png
	   :align: center

           The antenna is automatically stowed when the wind speed
           exceeds 60km/h.
