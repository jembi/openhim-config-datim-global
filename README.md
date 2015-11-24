OpenHIM config package - for DATIM Global
=========================================

This repo allows you to create a debian package that will automatically
configure the openhim-core server installed by the openhim-core debian package.

It has been configured specifically for the DATIM project. If you would like to
create a config package for the OpenHIM for your own project, then
[see here](https://github.com/jembi/openhim-config-pkg).

Getting started
---------------

Execute `.create-deb.sh` to create the package. This script will ask you if you
want to upload to launchpad or just create a .deb file.

When installed, the `load-initial-data.sh` script will be placed in `/etc/openhim/`
along with the data if you ever need to run it again.

After the package is installed the user must manually set the following:

* A DHIS username and password to use on the 'ADX/DXF import' channel under the
  'DHIS Global' route.
* The certificate for the 'DATIM-node' client must be added to the trusted list in
  the keystore.
