.. include:: /Includes.rst.txt

.. _typo3_conf_var_usage:


.. document title

#################
confval for TYPO3
#################

.. document subtitle

=======================================
Configure TYPO3 configuration variables
=======================================

The global configuration is stored in file
:file:`typo3conf/LocalConfiguration.php`.
This file overrides default settings from
:file:`typo3/sysext/core/Configuration/DefaultConfiguration.php`.


.. confval:: TYPO3_CONF_VARS

   :path: $GLOBALS
   :Usage: typo3_conf_var_usage
   :name: $GLOBALS['TYPO3_CONF_VARS']
   :type: confval_group

   This chapter describes this global configuration in more details and hints
   at other configuration possibilities.

.. confval:: BE

   :path: $GLOBALS > TYPO3_CONF_VARS
   :Usage: typo3_conf_var_usage
   :name: $GLOBALS['TYPO3_CONF_VARS']['BE']
   :type: confval_group

   Options related to the TYPO3 CMS backend.


.. confval:: FE

   :path: $GLOBALS > TYPO3_CONF_VARS
   :Usage: typo3_conf_var_usage
   :name: $GLOBALS['TYPO3_CONF_VARS']['FE']
   :type: confval_group

   Options related to the TYPO3 CMS backend.


.. confval:: requireMfa

   :path: $GLOBALS > TYPO3_CONF_VARS > BE
   :Usage: typo3_conf_var_usage
   :name: $GLOBALS['TYPO3_CONF_VARS']['BE']['requireMfa']
   :type: int
   :Default: 0
   :allowedValues: requireMfa-values

   Define users which should be required to set up multi-factor authentication.


.. confval-values:: requireMfa

   :shortdescription: 0 (no MFA), 1 (MFA for all users) - 4 (MFA for system maintainers)

   0:
      Default: Do not require multi-factor authentication
   1:
      Require multi-factor authentication for all users
   2:
      Require multi-factor authentication only for non-admin users
   3:
      Require multi-factor authentication only for admin users
   4:
      Require multi-factor authentication only for system maintainers

.. confval:: lockIP

   :path: $GLOBALS > TYPO3_CONF_VARS > BE
   :Usage: typo3_conf_var_usage
   :name: $GLOBALS['TYPO3_CONF_VARS']['BE']['lockIP']
   :type: int
   :Default: 0
   :allowedValues: lockIP-values

   Session IP locking for backend users. See :ref:`[FE][lockIP]<typo3ConfVars_fe_lockIP>` for details.


.. image:: Images/confval_output.png


.. confval:: lockIP

   :path: $GLOBALS > TYPO3_CONF_VARS > FE
   :Usage: typo3_conf_var_usage
   :name: $GLOBALS['TYPO3_CONF_VARS']['FE']['lockIP']
   :type: int
   :Default: 0
   :allowedValues: lockIP-values

   If activated, Frontend Users are locked to (a part of) their public IP
   (:php:`$_SERVER[REMOTE_ADDR]`) for their session, if REMOTE_ADDR is an
   IPv4-address. Enhances security but may throw off users that may change IP
   during their session (in which case you can lower it). The integer indicates
   how many parts of the IP address to include in the check for the session.


.. confval-values:: lockIP

   :shortdescription: 0 (no lock) - 5 (full IPv4 address)

   0
      Default Do not lock Frontend User sessions to their IP address at all
   1
      Use the first part of the visitors IPv4 address (for example "192.") as part
      of the session locking of Frontend Users
   2
      Use the first two parts of the visitors IPv4 address (for example "192.168")
      as part of the session locking of Frontend Users
   3
      Use the first three parts of the visitors IPv4 address
      (for example "192.168.13") as part of the session locking of Frontend Users
   4
      Use the visitors full IPv4 address (for example "192.168.13.84") as part of
      the session locking of Frontend Users (highest security)


You can lock IPs for backend users :confval:`$GLOBALS > TYPO3_CONF_VARS > BE > lockIP`
and for frontend users :confval:`$GLOBALS > TYPO3_CONF_VARS > FE > lockIP`.

Out of the box it is only possible require multi-factor authentication
for backend user by setting :confval:`$GLOBALS > TYPO3_CONF_VARS > BE > requireMfa`.
Possible values for this setting are :confval-values:`requireMfa`. We suggest
setting it to :confval-values:`requireMfa:1` when you have MFA enabled in your system.

Have a look at all configurations possible for the backend:
:confval:`$GLOBALS > TYPO3_CONF_VARS > BE > requireMfa`

There should be a hierarchical menu available:

.. figure:: Images/menu.png
   :class: with-border with-shadow
   :alt:   How the menu item should look like.

In the Index each value should be listed like this:


*  $GLOBALS

   *  TYPO3_CONF_VARS

*  TYPO3_CONF_VARS

   *  $GLOBALS > TYPO3_CONF_VARS

*  $GLOBALS > TYPO3_CONF_VARS

   *  FE
   *  BE

*  FE

   *   $GLOBALS > TYPO3_CONF_VARS > FE

*  BE

   *   $GLOBALS > TYPO3_CONF_VARS > BE

*  $GLOBALS > TYPO3_CONF_VARS > FE

   * lockIP

*  $GLOBALS > TYPO3_CONF_VARS > BE

   * lockIP
   * requireMfa

* lockIP

   *  $GLOBALS > TYPO3_CONF_VARS > FE > lockIP
   *  $GLOBALS > TYPO3_CONF_VARS > BE > lockIP

* requireMfa

   *  $GLOBALS > TYPO3_CONF_VARS > BE > requireMfa
