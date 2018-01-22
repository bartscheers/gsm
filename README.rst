The Global Sky Model
====================


The Global Sky Model (GSM) contains all sources from the VLSS, NVSS, and WENSS 
survey catalogs. 
For the LOFAR BBS calibration pipeline these tools can be used to create a sky model 
catalog file in ``makesourcedb`` format.
The ``gsm.py`` script
extracts sources in a cone of a given radius around a given position 
on the sky from the Global Sky Model database.

If you want to run the GSM database locally, you can get the 
catalog ``csv`` data from `here`_.

Be sure to install dependent packages, e.g., ``six``, ``numpy`` and
``pymonetdb``, and set ``$PYTHONPATH`` to the directory of installation.

Run gsm
-------

Before running the GSM scripts, copy ``template_config.cfg`` to ``config.cfg``
and fill in the database specifics, either for the local or remote 
GSM database.

The python wrapper script ``gsm.py`` can be used to generate a catalog file 
in ``makesourcedb`` format and can be run as:

``python gsm.py outfile RA DEC radius [vlssFluxCutoff [assocTheta]]``

Documentation
-------------

See the `LOFAR Imaging Cookbook`_ for more information.

.. _LOFAR Imaging Cookbook: https://support.astron.nl/LOFARImagingCookbook/
.. _here: https://homepages.cwi.nl/~bscheers/gsm/

