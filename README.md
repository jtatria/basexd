# basexd

BaseX Debian/Ubuntu daemon support using Java Service Wrapper

Script and conf file for starting and stopping BaseX as a system daemon.

## Dependencies:

BaseX, either from Debian/Ubuntu repos or from the BaseX website (debian pkg name: basex)
Java Service Wrapper, from Debian/Ubuntu repos as we are using debian templates (debian pkg name: service-wrapper)

Also, the daemon script assumes a daemon system user named basex, with rw access to a basex homedir at /var/lib/basex

To install in debian/ubuntu:

* Install dependencies:
  `sudo apt-get install basex service-wrapper`

* Create daemon user and group:
  `sudo addgroup --quiet --system basex`
  `sudo adduser --quiet --system --ingroup basex --home="/var/lib/basex" --no-create-home --disabled-password basex`

* Create daemon dir and set permissions
  `sudo mkdir /var/lib/basex`
  `sudo chown basex:basex /var/lib/basex`

* Copy "wrapper.conf" to /var/lib/basex:
  `sudo cp /path/to/wrapper.conf /var/lib/basex/`

* Run the daemon with:
  `sudo /path/to/basexd start`

* Install the basex service in init.d with
  `sudo /path/to/basexd install`

TODO: standardize file paths and locations. Remove hardcoded references. Generally Debianize, etc.
