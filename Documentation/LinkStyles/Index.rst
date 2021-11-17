.. include:: /Includes.rst.txt
.. highlight:: rst

============
Links styles
============

.. contents:: This page
   :backlinks: top
   :class: compact-list
   :depth: 99
   :local:


Various
=======

Within a page
-------------

Source::

   Defining a _`target`.

Rendering:

   Defining a _`target`.

Source::

   Linking to that `target`_.

Rendering:

   Linking to that `target`_.


External links, outside TYPO3 universe
--------------------------------------

The domain names https://example.com, https://example.net, https://example.org,
and https://example.edu are
second-level domain names in the Domain Name System of the Internet. They are
reserved by the Internet Assigned Numbers Authority (IANA) at the direction of
the Internet Engineering Task Force (IETF) as special-use domain names for
documentation purposes.

Expected:

.. code-block:: html

   <a class="reference external" href="https://example.com" rel="nofollow noopener">https://example.com</a>
   <a class="reference external" href="https://example.net" rel="nofollow noopener">https://example.net</a>
   <a class="reference external" href="https://example.org" rel="nofollow noopener">https://example.org</a>
   <a class="reference external" href="https://example.edu" rel="nofollow noopener">https://example.edu</a>


External links, inside TYPO3 universe
-------------------------------------

*  https://typo3.org/
*  https://typo3.com/
*  https://docs.typo3.org/

Expected:

.. code-block:: html

   <a class="reference external" href="https://typo3.org/">https://typo3.org/</a>
   <a class="reference external" href="https://typo3.com/">https://typo3.com/</a>
   <a class="reference external" href="https://docs.typo3.org/">https://docs.typo3.org/</a>


Other
=====

In :file:`conf.py` we have:

.. code-block:: python

   extlinks = {}
   extlinks["forge"] = ("https://forge.typo3.org/issues/%s", "Forge #")
   extlinks["issue"] = ("https://forge.typo3.org/issues/%s", "Issue #")
   extlinks["review"] = ("https://review.typo3.org/%s", "Review #")


Source::

   Let's link to `various`_.

Result:

   Let's link to `various`_.


Source::

   \|  :issue:`12345`  \|  `12345`:issue:
   \|  :forge:`345`    \|  `345`:forge:
   \|  :review:`567`   \|  `567`:forge:
   \|

Rendering:

   \|  :issue:`12345`  \|  `12345`:issue:
   \|  :forge:`345`    \|  `345`:forge:
   \|  :review:`567`   \|  `567`:forge:
   \|


Define in :file:`Settings.cfg`:

.. code-block:: ini

   [extlinks]
   #
   # ; These defaults are set in conf.py
   #
   # ; Example:
   # ;    :forge:`12345` will be rendered as
   # ;    <a href="https://forge.typo3.org/issues/12345">forge:12345</a>
   #
   # ; name = url | prefix
   #
   forge      = https://forge.typo3.org/issues/%s         | forge:
   review     = https://review.typo3.org/%s               | review:
   issue      = https://forge.typo3.org/issues/%s"        | Issue #
   t3ext      = https://extensions.typo3.org/extension/%s | t3ext:
   t3ext1     = https://extensions.typo3.org/extension/%s | ↗t3ext:
   t3ext2     = https://extensions.typo3.org/extension/%s | t3ext↗:
   t3ext3     = https://extensions.typo3.org/extension/%s | t3ext↗
   t3ext4     = https://extensions.typo3.org/extension/%s | t3ext:↗
   packagist  = https://packagist.org/packages/%s         | pckg:
   packagist1 = https://packagist.org/packages/%s         | ↗pckg:
   packagist2 = https://packagist.org/packages/%s         | pckg↗:
   packagist3 = https://packagist.org/packages/%s         | pckg↗
   packagist4 = https://packagist.org/packages/%s         | pckg:↗


Source::

   \|  :t3ext:`news`
   \|  :t3ext1:`news`
   \|  :t3ext2:`news`
   \|  :t3ext3:`news`
   \|  :t3ext4:`news`
   \|

   \|  :packagist:`georgringer/news`
   \|  :packagist1:`georgringer/news`
   \|  :packagist2:`georgringer/news`
   \|  :packagist3:`georgringer/news`
   \|  :packagist4:`georgringer/news`
   \|
Rendering:

   \|  :t3ext:`news`
   \|  :t3ext1:`news`
   \|  :t3ext2:`news`
   \|  :t3ext3:`news`
   \|  :t3ext4:`news`
   \|

   \|  :packagist:`georgringer/news`
   \|  :packagist1:`georgringer/news`
   \|  :packagist2:`georgringer/news`
   \|  :packagist3:`georgringer/news`
   \|  :packagist4:`georgringer/news`
   \|
