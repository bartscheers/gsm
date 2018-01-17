The Global Sky Model
====================


The Global Sky Model (GSM) contains all sources from the VLSS, NVSS, and WENSS 
survey catalogs. 
For the LOFAR BBS calibration pipeline these tools can be used to create a sky model 
catalog file in ``makesourcedb`` format.
The ``rungsm.py`` script, formerly known as ``gsm.py``, 
extracts sources in a cone of a given radius around a given position 
on the sky from the Global Sky Model database.
For more detail you are referred to the `LOFAR Imaging Cookbook`_.

If want to run the GSM database locally, you can get the 
catalog ``csv`` data from `here`_.

Be sure to install dependent packages ``six``, ``numpy`` and
``pymonetdb``.

Run gsm
-------

Before running the GSM scripts, copy ``template_config.cfg`` to ``config.cfg``
and fill in the database specifics.

The python wrapper script ``rungsm.py`` can be used to generate a catalog file 
in ``makesourcedb`` format and can be run as:

``python rungsm.py outfile RA DEC radius [vlssFluxCutoff [assocTheta]]``

.. _LOFAR Imaging Cookbook: https://support.astron.nl/LOFARImagingCookbook/
.. _here: https://homepages.cwi.nl/~bscheers/gsm/

