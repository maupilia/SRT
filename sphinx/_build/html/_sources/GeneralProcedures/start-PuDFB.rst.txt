.. SRT procedures documentation master file, created by
   sphinx-quickstart on Mon Aug  7 16:44:28 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


.. toctree::
   :maxdepth: 1


.. _start-PuDFB:

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

    ``> setupCCB`` |logo| :numref:`srt_receivers`  |logo| :numref:`srt_ACU_green`

    ``> goTo=*,85d`` |logo| :numref:`srt_mount`

#. Follow the link below to perform the pointing optimization:

    :ref:`pointing-focus`



On PULSAR/VLBI
---------------

#. Login as pulsar. Place your schedules in folder /home/pulsar/scheds/[your project code]

#. From a terminal, start SEADAS

    ``$ seadas``

#. On another workspace, open a new terminal and start a vnc session for corr@psrdfb:

    ``$ vncviewer psrdfb:2``

#. Type password at prompt.

In the vnc session corr@psrdfb
----------------------------------

#. Open a terminal and check the system clock is working properly (time properly synchronized, tick phase ~ 100 ns, positive or negative) by typing

    ``$ atdc``

#. If DFBCONTROLLER is not already on, open a new terminal and start it

    ``$ dfbcontroller``

#. In DFBCONTROLLER window, check that the colored label at the right of the "tkds" label is green and displays the word "CONNECTED". If not, click on it.

Inside SEADAS window
----------------------------------

#. Enable the antenna control by clicking on the red label at the top right corner of the Antenna and Pointing Management frame. |logo| :numref:`seadas_disabled`

#. Check that the label becomes green and displays the word "ENABLED" |logo| :numref:`seadas_enabled`

#. Select "Schedule" in the "Session mode" combo box |logo| :numref:`session_mode`

#. Click "Schedule Management". A window named "Seadas schedule management" pops up |logo| :numref:`schedule_management`

#. Click "Load sched" in "Schedule management" window. A system window pops up for browsing system directories and selecting the schedule file

#. In "Schedule manager" window select schedule lines to be done - mouse left click on each single line - or click button "Select all" for loading the entire schedule in the "Observations List" window |logo| :numref:`schedule_management_full`

#. If necessary, rearrange the order of the observations in the "Observations List" window  - left button click == cut line ; mid button click == paste line

#. Back on SEADAS main window click "Observe"

#. Do not forget to verify and adjust attenuation levels. You can find the test schedule TEST.scd under the directory scheds/ (or you can add a similar line to your schedule). Once you have started the schedule, check the PDFB3 panel in the psrdfb vnc session, Under tab `Samplers` where you fill find the the RMS levels of the channels. Also, check the SPD plotting tool to compare the bandpasses of the two channel. Aim to align the bandpasses, with the highest channel RMS around 13. In order to do so, iteratively go back to the SEADAS interface and select the desired attenuation values (which can be different for the two channels), then press `set atten.`
