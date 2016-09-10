Alignak NSCA receiver Module
============================

*Alignak NSCA module for the Alignak Receiver*

Build status (stable release)
----------------------------------------

.. image:: https://travis-ci.org/Alignak-monitoring-contrib/alignak-module-nsca.svg?branch=master
    :target: https://travis-ci.org/Alignak-monitoring-contrib/alignak-module-nsca


Build status (development release)
----------------------------------------

.. image:: https://travis-ci.org/Alignak-monitoring-contrib/alignak-module-nsca.svg?branch=develop
    :target: https://travis-ci.org/Alignak-monitoring-contrib/alignak-module-nsca


Short description
-------------------

This module for Alignak receiver reads and decodes NSCA passive notifications to dispatch them into the Alignak framework.


Configuration
-------------------

Once installed, this module has its own configuration file in the */usr/local/etc/alignak/arbiter_cfg/modules* directory.
The default configuration file is *mod-nsca.cfg*. This file is commented to help configure all the parameters.

The default configuration is convenient for 'recent' NSCA client implementing NSCA version 3.

This configuration has been tested with Linux send_nsca 2.9.1 and Windows NSClient most recent versions (from 0.4.1).

.. note::  Received NSCA packets which are not containing version 3 information are dropped by the module!

To configure Alignak receiver to use this module:

    - edit your receiver daemon configuration file
    - add the `module_alias` parameter value (nsca) to the `modules` parameter of the daemon

To set up several NSCA listeners:

    - copy the default configuration to another file,
    - change the module alias parameter
    - change the listening port
    - edit your receiver daemon configuration file
    - add the new `module_alias` parameter value to the `modules` parameter of the daemon


Known limitations
-------------------

.. note::  The NSCA module implementation is currently limited to the "xor" obfuscation/encryption.



Bugs, issues and contributing
----------------------------------------

Please report any issue using the project `GitHub repository: <https://github.com/Alignak-monitoring-contrib/alignak-module-nsca/issues>`_.

License
----------------------------------------

Alignak Backend Modules is available under the `GPL version 3 <http://opensource.org/licenses/GPL-3.0>`_.

