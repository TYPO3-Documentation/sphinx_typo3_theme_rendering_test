.. include:: /Includes.rst.txt

============
Replacements
============

.. contents:: This page
   :backlinks: top
   :class: compact-list
   :depth: 99
   :local:


Sphinx defaults
===============

These replacements are always available in Sphinx:

===================== ==========================
Notation              Result
===================== ==========================
`|today|`             |today|
`|release|`           |release|
`|version|`           |version|
===================== ==========================

Provided by 'sphinxcontrib-docstypo3'
=====================================

The following replacements are made available by the
'sphinxcontrib-docstypo3' Sphinx extension. The actual values for this project
are shown.

=============================  =================================
Notation                       Result
=============================  =================================
`|cfg_audience|`                  |cfg_audience|
`|cfg_author|`                    |cfg_author|
`|cfg_t3author|`                  |cfg_t3author|
`|cfg_copyright|`                 |cfg_copyright|
`|cfg_description|`               |cfg_description|
`|cfg_language|`                  |cfg_language|
`|cfg_license|`                   |cfg_license|
`|cfg_maintainer|`                |cfg_maintainer|
`|cfg_project|`                   |cfg_project|
`|cfg_published|`                 |cfg_published|
`|cfg_release|`                   |cfg_release|
`|cfg_version|`                   |cfg_version|

# urls
`|hto_project_contact|`           |hto_project_contact|
`|hto_project_discussions|`       |hto_project_discussions|
`|hto_project_home|`              |hto_project_home|
`|hto_project_issues|`            |hto_project_issues|
`|hto_project_repository|`        |hto_project_repository|
=============================  =================================

Use :file:`Settings.cfg` for configuration:

.. code-block:: ini

   [general]

   # everything here goes to 'conf.py'

   audience =
   author =
   copyright =
   description =
   language =
   license =
   maintainer =
   project =
   published =
   release =
   version =


   [html_theme_options]
   project_contact     =  # url or empty
   project_discussions =  # url or empty
   project_home        =  # url or empty
   project_issues      =  # url or empty
   project_repository  =  # url or empty


Example: Reconstruct 'Settings.cfg'
-----------------------------------

**Documentation source (rst):**

.. code-block:: rst

   .. parsed-literal::

      [general]

      # prefix in replacements: cfg
      # everything here goes to 'conf.py'

      audience    = |cfg_audience|
      author      = |cfg_author|
      t3author    = |cfg_t3author|
      copyright   = |cfg_copyright|
      description = |cfg_description|
      language    = |cfg_language|
      license     = |cfg_license|
      maintainer  = |cfg_maintainer|
      project     = |cfg_project|
      published   = |cfg_published|
      release     = |cfg_release|
      version     = |cfg_version|


      [html_theme_options]

      # prefix in replacements: hto

      project_contact     = |hto_project_contact|
      project_discussions = |hto_project_discussions|
      project_home        = |hto_project_home|
      project_issues      = |hto_project_issues|
      project_repository  = |hto_project_repository|


**Rendering result:**

.. parsed-literal::

   [general]

   # prefix in replacements: cfg
   # everything here goes to 'conf.py'

   audience    = |cfg_audience|
   author      = |cfg_author|
   t3author    = |cfg_t3author|
   copyright   = |cfg_copyright|
   description = |cfg_description|
   language    = |cfg_language|
   license     = |cfg_license|
   maintainer  = |cfg_maintainer|
   project     = |cfg_project|
   published   = |cfg_published|
   release     = |cfg_release|
   version     = |cfg_version|


   [html_theme_options]

   # prefix in replacements: hto

   project_contact     = |hto_project_contact|
   project_discussions = |hto_project_discussions|
   project_home        = |hto_project_home|
   project_issues      = |hto_project_issues|
   project_repository  = |hto_project_repository|


About the settings
==================

*Note:* Choose only one of the example lines for :file:`Settings.cfg`.

.. confval:: |cfg_audience|

   Will be replaced by the value of `audience` as defined in :file:`conf.py`
   or the empty string.

   Example definition in :file:`Settings.cfg`::

      [general]

      audience = developers, power users
      audience = Everybody interested


.. confval:: |cfg_author|

   Will be replaced by the value of `author` as defined in :file:`conf.py`.
   If empty, `t3author` will be used. If none is found, the empty string is
   used.

   Example definition in :file:`Settings.cfg`::

      [general]

      author = TYPO3 Documentation Team
      author = Ernest Hemingway <ernest@example.org>, Oscar Wilde


.. confval:: |cfg_t3author|

   Deprecated.


.. confval:: |cfg_copyright|

   Will be replaced by the value of `copyright` as defined in :file:`conf.py`
   or the empty string.

   Example definition in :file:`Settings.cfg`::

      [general]

      copyright = 2021 by the authors



.. confval:: |cfg_description|

   Will be replaced by the value of `description` as defined in :file:`conf.py`
   or the empty string.

   Example definition in :file:`Settings.cfg`::

      [general]

      description =

      description = ...

      description =
         This is the documentation of TYPO3's system extension 'adminpanel'. It
         displays a bar at the bottom of the screen on the frontend, from which you
         can access information per page.



.. confval:: |cfg_language|

   Will be replaced by the value of `language` as defined in :file:`conf.py`
   or the empty string.

   ((Let's see what the output of this is. `language` may be a built in value.))


.. confval:: |cfg_license|

   Will be replaced by the value of `license` as defined in :file:`conf.py`
   or the empty string.

   Example definition in :file:`Settings.cfg`::

      [general]

      license = CC-BY 4.0
      license = https://creativecommons.org/licenses/by/4.0/
      license = CC-BY 4.0 <https://creativecommons.org/licenses/by/4.0/>
      license = MIT


.. confval:: |cfg_maintainer|

   Will be replaced by the value of `maintainer` as defined in :file:`conf.py`
   or the empty string.

   Example definition in :file:`Settings.cfg`::

      [general]

      maintainer = "John Doe <john.doe@example.org>"


.. confval:: |cfg_project|

   Will be replaced by the value of `project` as defined in :file:`conf.py`
   or the empty string.

   Example definition in :file:`Settings.cfg`::

      [general]

      project = extkey
      project = News
      project = adminpanel
      project = Core changelog



.. confval:: |cfg_release|

   Will be replaced by the value of `release` as defined in :file:`conf.py`
   or the empty string.

   Example definition in :file:`Settings.cfg`::

      [general]

      release = 1.2.3
      release = v1.2.dev3
      release = main
      release = develop


.. confval:: |cfg_version|

   Will be replaced by the value of `version` as defined in :file:`conf.py`
   or the empty string.

   Example definition in :file:`Settings.cfg`::

      [general]

      version = 1.2
      version = main
      version = develop

