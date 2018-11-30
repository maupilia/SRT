.. SRT procedures documentation master file, created by
   sphinx-quickstart on Mon Aug  7 16:44:28 2017.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


.. toctree::
   :maxdepth:1
  
.. _start-CoLSa:

Start the observations
======================

$ : commands to insert in a shell   
 
> : commands to insert in the operatorInput panel

.. |logo| image:: monocle_.png 
..    :width: 20pt
..    :height: 20pt
..   :align: left
|logo|: check on the monitor


======================


#. Insert your project number 

    ``> project=[projectID]`` |logo| :numref:`srt_scheduler`

#. Initial setup 

    ``> antennaReset`` |logo| :numref:`srt_ACU_axis_blocked` 

    ``> setupLLP``  |logo| :numref:`srt_receivers_KKG` |logo| :numref:`srt_ACU_green`

#. Select the active surface shape (Parabolic for L-band observations)

    ``> asSetup=P`` |logo| :numref:`srt_as_parabolic`

#. Select the receiver mode 

    ``> receiversMode=[code]`` where ``[code]`` can be ``XXC1``,
    ``XXC2``, ``XXC3``, ``XXC4``, ``XXC5``, ``XXL1``, ``XXL2``,
    ``XXL3``, ``XXL4``, ``XXL5``.

       - **C** is for **Circular**, **L** for **Linear polarization** ;
       - **1** : all band, 1300-1800 MHz (no filter) ;
       - **2** : 1320-1780 MHz ;
       - **3** : 1350-1450 MHz ;
       - **4** : 1300-1800 MHz (band-pass) ;
       - **5** : 1625-1715 MHz.

#. Select the Maccaferri filter :
    
    - ``ifd=BW-NARROW`` for 115 MHz of bw ;
    - ``ifd=BW-MEDIUM`` for 230 MHz of bw ;
    - ``ifd=BW-WIDE`` for 460 MHz of bw ;
    - ``ifd=BW-UNFILTERED``.


#. Insert the Local Oscillator value in MHz

    ``> setLO=[freq]`` |logo| :numref:`srt_receivers_LLP`

#. Select and configure the SARDARA backend in L-band

    ``> chooseBackend=Sardara`` |logo| :numref:`srt_scheduler`
    
    ``$ genericBackendTui BACKENDS/Sardara``

    ``> initialize=SL00S`` for full Stokes observations or
    ``> initialize=SL00`` for non full Stokes observations.


#. Set the different parameters of the backend 

    ``> setSection=[sect],*,1500,*,*,3000,[bin]`` |logo| :numref:`srt_genericBackend`

     with : 

       - ``[sect]`` : 0 in full Stokes observations and ``[sect]`` :
         0, 1 in non full-stokes observations ;
       - ``[bin]`` the frequency channels (1024 or 16384).

    
#. Choose the integration time in ms (e.g. n=10 corresponds to 100 spectra/sec)

    ``> integration=[n]``

#. Put the antenna at 45 deg of elevation before to check that the signal is in the linear range of the backend:

    ``> goTo=*,45d`` |logo| :numref:`srt_mount`

#. Attenuate the signal based on the rms range [30;33] and check the value on the interface

    ``> getRms``  

    ``> setAttenuation=[sect],[att]``    with [att] the attenuation from 0 to 15 dB. |logo| :numref:`srt_genericBackend`

#. Check the tsys (typical values to be inserted)

     ``> tsys`` |logo| :numref:`srt_genericBackend`

#. Begin the schedule by indicating the start scan [N] or subscan [N_n] in the SCD file 

     ``> startSchedule=[schedulename].scd,[N]`` |logo| :numref:`srt_scheduler`
