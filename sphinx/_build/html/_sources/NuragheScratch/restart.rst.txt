.. SRT procedures documentation master file, created by
   sphinx-quickstart on Mon Aug  7 16:44:28 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

===================
Restart Nuraghe
===================

Please, follow the steps in the order.

#. On **nuraghe-mng**, go on the MNG virtual desktop. Open a shell and launch Nuraghe.

    ``nuragheConsole -start``

    The ACS Command Center will appear.


#. In the *Common Settings* section located on the upper left of the ACS interface, select 

    ``localhost(single-machine project)``


#. In the *Acs Suite* section, click on  ``Start`` (green triangle with Start).


#. On the bottom left of the ACS interface, click on the ``ACS`` tab. Wait about one minute to check that the system is running. When it is ready, the following message appears **ACS is up and running** in the log tab of ACS.


#. In the *Containers* section, click on the single green triangles to start each container. It is not necessary to wait for the closing of the Deployment info window of each container. The name of the containers appear progressively in the log tab with the message ``ContainerStatusMsg: Ready``. 


#. On **nuraghe-AS**, open two shells if they are not already there. On the first one, write 

    ``asContainers``

    On the second one, write  ``SRTActiveSurfaceGUIClient &``

    The graphical interface of the active surface appears. The active
    surface is ready when it is green (it takes several minutes).


#. On **nuraghe-mng**, check that the you have now **31 containers**.


#. Go on the CONSOLE virtual desktop of **nuraghe-mng**. Open a shell and execute the following command

    ``nuragheConsole``

    Eight panels appear:

     - **operatorInput** (:numref:`srt_operatorinput`)
     - **AntennaBoss** (:numref:`srt_antennaboss`)
     - **GenericBackend** (:numref:`srt_genericBackend`)
     - **Mount** (:numref:`srt_mount_ok`)
     - **Observatory** (:numref:`srt_observatory`)
     - **Receivers** (:numref:`srt_receivers`)
     - **Scheduler** (:numref:`srt_scheduler`)
     - **MinorServo** (:numref:`srt_minorservo`)


Nuraghe is now ready! 
