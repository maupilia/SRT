.. SRT procedures documentation master file, created by
   sphinx-quickstart on Mon Aug  7 16:44:28 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

===================
Shutdown of Nuraghe
===================

Please, follow the steps in the indicated order.

#. On **nuraghe-mng**, open a shell on the CONSOLE virtual desktop and close the Nuraghe console

    ``nuragheConsole --stop``

#. On **nuraghe-AS**, close the graphical interface of the active surface with a click on the ``Quit`` button (bottom right)

#. On **nuraghe-mng**, go on the ACS Command Center, which is in the MANAGER virtual desktop. Click on the collective stop button ``(black square)`` located under the list of all of the containers to close them. It is also possible to close each container individually.

#. On **nuraghe-AS**, select one of the shells that is already open and write ``enter`` to check you have the control of the prompt. In the case you do not have the prompt, press ``ctrl-c``. Then, execute the following commands (you can use the upper arrow of the keyboard to find the commands)

    ``~/SRTStopActiveSurfaceContainer.sh``

   then ``killACS``.

#. On **nuraghe-mng**, go back on the ACS Command Center and close **ACS  Suite** with a click on the corresponding stop button ``(black square with stop)``.

#. On a shell of **nuraghe-mng**, kill the remaining ACS processes

    ``killACS``

   and wait the following message: **Removing ACS_INSTANCE temporary directories … done**.
