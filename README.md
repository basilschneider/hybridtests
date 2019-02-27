Hybrid testing
==============

This repository is for testing the CMS Outer Tracker Phase-2 hybrid prototypes.
It currently only supports the testing of 8CBC2 hybrids. Other hybrid prototypes
might be added in the future.

The repository contains
1) A bash script that walks the user through a hybrid test
2) The results from tested hybrids


Installation
============

To use this repository, one needs to set up the Middleware (Ph2_ACF) first. The
Middleware can be found under:
https://gitlab.cern.ch/cms_tk_ph2/Ph2_ACF

Be sure to use the right branch, e.g. to test a CBC2 hybrid with a GLIB setup,
you want to use the Middleware that supports GLIB and CBC2, not FC7 and CBC3.

To use this script go to the middleware directory, get a kerberos ticket for
authentication, clone this repository and make a symlink.
```bash
cd Ph2_ACF
kinit <username>@CERN.CH
git clone https://:@gitlab.cern.ch:8443/bschneid/hybridtests.git
ln -s hybridtests/measureHybrids .
```
If you cannot clone the repository due to authentication issues, please contact
me.

To start a measurement, simply do
```bash
./measurehybrids
```
inside the middleware directory.
