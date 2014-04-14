basexd
======

BaseX Debian/Ubuntu daemon support using Java Service Wrapper

Script and conf file for starting and stopping BaseX as a system daemon.

Dependencies:
BaseX, either from Debian/Ubuntu repos or from the BaseX website (debian pkg name: basex)
Java Service Wrapper, from Debian/Ubuntu repos as we are using debian templates (debian pkg name: service-wrapper)

Also, the daemon script assumes a daemon system user named basex, with rw access to a basex homedir at /var/lib/basex

TODO: standardize file paths and locations. Remove hardcoded references. Generally Debianize, etc.
