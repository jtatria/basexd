basexd
======

BaseX Debian/Ubuntu daemon support using Java Service Wrapper

Script and conf file for starting and stopping BaseX as a system daemon.

The script assumes that BaseX is installed, either from Debian/Ubuntu repos or from the BaseX website, and that a system daemon user called 'basex' has been creted with rw access to /var/lib/basex/*

TODO: standardize file paths and locations. Remove hardcoded references. Generally Debianize, etc.
