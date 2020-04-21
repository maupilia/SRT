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


On DISCOS-CONSOLE
------------------

#. Insert your project number

    ``> project=[projectID]``    |logo| :numref:`srt_scheduler`

#. Initial setup

    ``> antennaReset``   |logo| :numref:`srt_ACU_axis_blocked`

    ``> setupLLP`` |logo| :numref:`srt_receivers`  |logo| :numref:`srt_ACU_green`

    ``> goTo=*,85d`` |logo| :numref:`srt_mount`


On PULSAR/VLBI
---------------

#. Login as pulsar. Place your schedules in folder /home/pulsar/scheds/[your project code]

#. From a terminal, start SEADAS

    ``$ seadas``

#. On another workspace, open a new terminal and start a vnc session for the head node leap0:

    ``$ vncviewer leap0:2``


In the vnc session leap0
----------------------------------

#. If you do not see the LEAPCONTROLLER interface, open a new terminal and start it

    ``$ /home/user/seadas/bin/leapcontroller``


Inside SEADAS window
----------------------------------

#. Enable the antenna control by clicking on the red label at the top right corner of the Antenna and Pointing Management frame. |logo| :numref:`seadasDisabled`

#. Check that the label becomes green and displays the word "ENABLED"

#. Select "Schedule" in the "Session mode" combo box

#. Click "Schedule Management". A window named "Seadas schedule management" pops up

#. Click "Load sched" in "Schedule management" window. A system window pops up for browsing system directories and selecting the schedule file

#. In "Schedule manager" window select schedule lines to be done - mouse left click on each single line - or click button "Select all" for loading the entire schedule in the "Observations List" window

#. If necessary, rearrange the order of the observations in the "Observations List" window  - left button click == cut line ; mid button click == paste line

#. Back on SEADAS main window click "Observe"
