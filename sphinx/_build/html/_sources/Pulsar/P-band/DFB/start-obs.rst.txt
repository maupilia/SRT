.. SRT procedures documentation master file, created by
   sphinx-quickstart on Mon Aug  7 16:44:28 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


.. toctree::
   :maxdepth: 1

.. _start-PuPDF:

Start the observations
======================

$ : commands to insert in a shell

> : commands to insert in the operatorInput panel


On seadas
----------

Place your observing files in pulsar@seadas as follows:

   - your seadas setup and schedule file(s) in folder: pulsar@seadas:/home/pulsar/scheds/[your project code]


On discos-console
------------------

#. Insert your project number

    ``> project=[projectID]``

#. Initial setup

    ``> antennaReset``

    ``> setupPPP``

    ``> goTo=*,81.9d``


#. On a terminal open a vnc session for pulsar@seadas:

    ``$ vncviewer seadas:1``

#. If this fails, start a new vnc session on pulsar@seadas.

#. Type password at prompt.



#. On another workspace, open a new terminal and start a vnc session for corr@psrdfb:

    ``$ vncviewer psrdfb:2``

#. If this fails, start a new vnc session on corr@psrdfb.

#. Type password at prompt.


In the vnc session pulsar@seadas
----------------------------------

#. Open a terminal and start SEADAS

    ``$ seadas``

#. In the log frame of seadas main window check that SEADAS connects to nuraghe

#. Click on the red label at the top right corner of the Antenna and Pointing Management frame.

#. Check that the clicked label becomes green and dislpays the word "ENABLED"


In the vnc session corr@psrdfb
----------------------------------

#. Open a terminal and check the system clock is working properly (time properly synchronized, tick phase ~ 100 ns, positive or negative) by typing

    ``$ atdc``

#. Open a new terminal and start DFBCONTROLLER

    ``$ dfbcontroller``

#. In DFBCONTROLLER window, check that the colored label at the right of the
  "tkds" label is green and displays the word "CONNECTED". If not, click on it.


Inside SEADAS window
------------------------

#. Select "Schedule" in the "Session mode" combo box

#. Verify and adjust attenuation levels. You can do so by following the procedure below, using the schedule TEST.scd which you will find under the directory /home/corr/scheds/. Once you have started the schedule (see points below) you need to check the PDFB3 panel in the psrdfb vnc session. Under tab `...` make sure that the RMS level for each channel is around 10. If it is not, go back to the SEADAS interface and select different attenuation values (which can be different for the two channels) and press `set atten.`

#. Click "Schedule Management". A window named "Seadas Schedule Manager" pops up

#. Click "Load sched" in "Schedule Manager" window. A system window pops up for browsing system directories and selecting the schedule file

#. In "Schedule manager" window select schedule lines to be done - mouse left click on each single line - or click button "Select all" for loading the entire schedule in the "Observations List" window

#. If necessary, rearrange the order of the observations in the "Observations List" window  - left button click == cut line ; mid button click == paste line

#. Click "Observe"
