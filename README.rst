The Global Sky Model
====================


The Global Sky Model (GSM) contains all sources from the VLSS, TGSS, WENSS (main and polar)
and NVSS survey catalogs. 
For the LOFAR BBS calibration pipeline these tools can be used to create a sky model 
catalog file in ``makesourcedb`` format.
The ``gsm.py`` script
extracts sources in a cone of a given radius around a given position 
on the sky from the Global Sky Model database.

Run gsm.py
----------

Install the required packages. Best is to run the script in 
virtual env.

If you want to run your own GSM database (locally), you can get the 
catalog ``csv`` files from `here`_. 
Copy ``template_config.cfg`` to ``config.cfg``
and fill in the database parameters, either for the local or remote 
GSM database.

The python wrapper script ``gsm.py`` can be used to generate a catalog file 
in ``makesourcedb`` format and can be run as:

``python gsm.py [-d dbconfig] [-c config] [-v version] [-h help]``

The database configuration file and the gsm-parameters config file need to be copied
from the ``template_*.cfg`` files on ``gsm/config``. Default ``gsm.py`` will
look for the file in the working diectory.

Note that since the last version we introduced the ``basecat`` argument. This 
can be set in the gsm-parameters config file to 
either VLSS or TGSS as the base catalogue for which counterparts will
be searched in the other catalogues.

Run gsm script after ``pip install``
------------------------------------

In your virtualenv you can ``pip install gsm`` and then use
the ``bin/gsm`` script to run the GSM from the command line:

``gsm [-d dbconfig] [-c config] [-v version] [-h help]``

Documentation
-------------

See the `LOFAR Imaging Cookbook`_ for more information.

.. _LOFAR Imaging Cookbook: https://support.astron.nl/LOFARImagingCookbook/
.. _here: https://homepages.cwi.nl/~bscheers/gsm/

