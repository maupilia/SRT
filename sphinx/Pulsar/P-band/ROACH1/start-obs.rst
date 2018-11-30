.. SRT procedures documentation master file, created by
   sphinx-quickstart on Mon Aug  7 16:44:28 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


.. toctree::
   :maxdepth: 1


.. _start-PuPRO:

Start the observations
======================

$ : commands to insert in a shell

> : commands to insert in the operatorInput panel

.. |logo| image:: monocle_.png
..    :width: 20pt
..    :height: 20pt
..   :align: left
|logo|: check the execution on the monitor



On seadas
----------

Place your observing files in corr@seadas as follows:

   - your seadas setup file(s) in folder:    corr@seadas:/home/corr/setup/[your project code]

   - your seadas schedule file(s) in folder: corr@seadas:/home/corr/scheds/[your project code]



On mng-dev
------------------

#. Insert your project number

    ``> project=[projectID]``    |logo| :numref:`srt_scheduler`

#. Initial setup

    ``> antennaReset``   |logo| :numref:`srt_ACU_axis_blocked`

    ``> setupPLP`` |logo| :numref:`srt_receivers`  |logo| :numref:`srt_ACU_green`

    ``> goTo=*,81.9d`` |logo| :numref:`srt_mount`


#. On a terminal open a vnc session for corr@seadas:

    ``$ vncviewer seadas:1``

#. If this fails, start a new vnc session on corr@seadas.

#. Type password at prompt.



#. On another workspace, open a new terminal and start a vnc session for the head node leap0:

    ``$ vncviewer leap0:1``

If it is not active:

7. Log on to the LEAP cluster :

    ``$ ssh -X user@leap0``     *ask for password*


8. Launch a VNC session once logged on to leap0 :

    ``leap0: $ vncserver &``


In the vnc session corr@seadas
----------------------------------

#. If you do not see the SEADAS interface, open a terminal and start it:

    ``$ seadas``

#. In the log frame of seadas main window check that SEADAS connects to nuraghe

#. Click on the red label at the top right corner of the Antenna and Pointing Management frame.

#. Check that the clicked label becomes green and dislpays the word "ENABLED"


In the vnc session leap0
----------------------------------

#. If you do not see the LEAPCONTROLLER interface, open a new terminal and start it

    ``$ leapcontroller``

#. In LEAPCONTROLLER window, check that the colored label at the right of the "..." label is green and displays the word "CONNECTED". If not, click on it.


Inside SEADAS window
------------------------

#. Select "Schedule" in the "Session mode" combo box

#. Verify and adjust attenuation levels. You can do so by following the procedure below, using the schedule TEST.scd which you will find under the directory /home/corr/scheds/. Once you have started the schedule (see points below) you need to check the PDFB3 panel in the psrdfb vnc session. Under tab `...` make sure that the RMS level for each channel is around 10. If it is not, go back to the SEADAS interface and select different attenuation values (which can be different for the two channels) and press `set attn.`

#. Click "View obs list". A window named "Observations List" pops up

#. Click "View schedule". A window named "Schedule Manager" pops up

#. Click "Load sched" in "Schedule Manager" window. A system window pops up for browsing system directories and selecting the schedule file

#. In "Schedule manager" window select schedule lines to be done - mouse left click on each single line - or click button "Select all" to load the entire schedule in the "Observations List" window

#. If necessary, rearrange the order of the observations in the "Observations List" window  - left button click == cut line ; mid button click == paste line

#. Click "Observe"
