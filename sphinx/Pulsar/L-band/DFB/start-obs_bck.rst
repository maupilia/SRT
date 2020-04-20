.. SRT procedures documentation master file, created by
      sphinx-quickstart on Mon Aug  7 16:44:28 2017.
         You can adapt this file completely to your liking, but it should at least
	    contain the root `toctree` directive.


	    .. toctree::
	          :maxdepth: 1

			     .. _startPuLDF:

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

						    ``> setupLLP``

						        ``> goTo=*,85d``


							On viewer01
							-------------

							#. Login as pulsar, open a terminal and start SEADAS

							       ``$ seadas``



							       #. On another workspace, open a new terminal and start a vnc session for corr@psrdfb:

								      ``$ vncviewer psrdfb:2``

								      #. Type password at prompt.


									 In the vnc session corr@psrdfb
									 ----------------------------------

									 #. Open a terminal and check the system clock is working properly (time properly synchronized, tick phase ~ 100 ns, positive or negative) by typing

									        ``$ atdc``

										#. If DFBCONTROLLER is not already open, open a new terminal and start it

										       ``$ dfbcontroller``

										       #. In DFBCONTROLLER window, check that the colored label at the right of the
											    "tkds" label is green and displays the word "CONNECTED". If not, click on it.


											    Inside SEADAS window
											    ----------------------------------

											    #. Enable the antenna by clicking on the red label at the top right corner of the Antenna and Pointing Management frame.

											       #. Check that the label becomes green and displays the word "ENABLED"

												  #. Select "Schedule" in the "Session mode" combo box

												     #. Click "Schedule Management". A window named "Seadas schedule management" pops up

													#. Click "Load sched" in "Schedule management" window. A system window pops up for browsing system directories and selecting your schedule file

													   #. In "Schedule manager" window select schedule lines to be done - mouse left click on each single line - or click button "Select all" for loading the entire schedule in the "Observations List" window

													      #. If necessary, rearrange the order of the observations in the "Observations List" window  - left button click == cut line ; mid button click == paste line

														 #. On seadas main window lick "Observe"

														    #. Do not forget to verify and adjust attenuation levels. You can do so by following the procedure below, using the schedule TEST.scd which you will find under the directory /home/pulsar/scheds/. Once you have started the schedule (see points below) you need to check the PDFB3 panel in the psrdfb vnc session. Under tab `...` make sure that the RMS level for each channel is around 10. If it is not, go back to the SEADAS interface and select different attenuation values (which can be different for the two channels) and press `set atten.`
