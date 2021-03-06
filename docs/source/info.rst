
More Information
################

Functionally based on pvMail UNIX shell script written in 1999.

Summary
*******

Watches an EPICS PV and sends email when it changes from 0 to 1.
PV value can be either integer or float.

.. note::
   When "running", wait for trigger PV to go from 0 to 1.  When that
   happens, fetch mail message from message PV.  Then, send that
   message out to each of the email addresses.  The message 
   content is prioritized for view on a small-screen device such 
   as a pager or a PDA or smartphone.


.. _svn.repo:

version control repository
**************************

The PvMail project is hosted on GitHub (https://github.com/prjemian/pvMail).
You may check out the entire project source code 
:index:`github repository`::

	git clone  https://github.com/prjemian/pvMail

GitHub has additional advice for alternative methods.


Documentation
*************

.. index:: 
    PvMail project

Documentation for the PvMail project, 
maintained using Sphinx (http://sphinx.pocoo.org),
is available from:

* http://PvMail.readthedocs.org


.. index:: TODO items

.. _TODO:

TODO items for future releases
##############################

:see: https://github.com/prjemian/pvMail/issues


Authors
#######

:author: Kurt Goetze (original version)
:author: Pete Jemian (this version)
:organization: AES/BCDA, Advanced Photon Source, Argonne National Laboratory



Requirements
############

:requires: EPICS system (http://www.aps.anl.gov/epics) 
    with at least two process variables (PVs)
    where the "Trigger PV" toggles between values of 0 and 1
    and the "SendMessage PV" contains a string to send as part of 
    the email message.
:requires: PyEpics (http://cars9.uchicago.edu/software/python/pyepics3/)
:requires: PyQt4 (https://wiki.python.org/moin/PyQt)
