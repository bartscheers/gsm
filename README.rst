The Global Sky Model
====================

Before running, the catalogs need to be loaded. 
Get them from https://homepages.cwi.nl/~bscheers/gsm/

Run gsm
-------

Also before running, copy ``template_config.cfg`` to ``config.cfg``
and specify the database connection values.

The python wrapper script ``rungsm.py`` can be used to generate a catalog file 
in ``makesourcedb`` format and can be run as:

``python rungsm.py outfile RA DEC radius [vlssFluxCutoff [assocTheta]]``


