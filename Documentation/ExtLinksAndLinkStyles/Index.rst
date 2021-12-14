.. include:: /Includes.rst.txt
.. highlight:: rst

========================
ExtLinks and Link styles
========================

.. contents:: This page
   :backlinks: top
   :class: compact-list
   :depth: 99
   :local:



ExtLinks
========

In :file:`conf.py` we have:

.. code-block:: python

   extlinks = {}
   extlinks["forge"] = ("https://forge.typo3.org/issues/%s", "Forge #")
   extlinks["issue"] = ("https://forge.typo3.org/issues/%s", "Issue #")
   extlinks["review"] = ("https://review.typo3.org/%s", "Review #")


Defined in :file:`Settings.cfg`:

.. code-block:: ini

   [extlinks]

   forge       = https://forge.typo3.org/issues/%s         | forge:
   forge2      = https://forge.typo3.org/issues/%s         | forge#
   forge3      = https://forge.typo3.org/issues/%s         | forge↗#
   forge4      = https://forge.typo3.org/issues/%s         | forge:#
   issue       = https://forge.typo3.org/issues/%s"        | forge:
   packagist   = https://packagist.org/packages/%s         | pckg↗
   packagist3  = https://packagist.org/packages/%s         | pckg:
   packagist4  = https://packagist.org/packages/%s         | PCKG:
   review      = https://review.typo3.org/%s               | review:
   t3ext       = https://extensions.typo3.org/extension/%s | t3ext↗
   t3ext2      = https://extensions.typo3.org/extension/%s | ext↗
   t3ext3      = https://extensions.typo3.org/extension/%s | ext:
   t3ext4      = https://extensions.typo3.org/extension/%s | EXT:
   theme-issue = https://github.com/TYPO3-Documentation/sphinx_typo3_theme/issues/%s | theme issue #

Source::

   ====================== ========================= =========================
   Notation               Alt-notation              Result
   ====================== ========================= =========================
   ``:issue:`12345```     ```12345`:issue:``        :issue:`12345`
   ``:forge:`345```       ```345`:forge:``          :forge:`345`
   ``:forge2:`345```      ```345`:forge2:``         :forge2:`345`
   ``:forge3:`345```      ```345`:forge3:``         :forge3:`345`
   ``:forge4:`345```      ```345`:forge4:``         :forge4:`345`
   ``:review:`567```      ```567`:review:``         :review:`567`
   ``:t3ext:`news```      ```news`:t3ext:``         :t3ext:`news`
   ``:t3ext2:`news```     ```news`:t3ext2:``        :t3ext2:`news`
   ``:t3ext3:`news```     ```news`:t3ext3:``        :t3ext3:`news`
   ``:t3ext4:`news```     ```news`:t3ext4:``        :t3ext4:`news`
   ``:packagist:`news```  ```news`:packagist:``     :packagist:`news`
   ``:packagist3:`news``` ```news`:packagist3:``    :packagist3:`news`
   ``:packagist4:`news``` ```news`:packagist4:``    :packagist4:`news`
   ====================== ========================= =========================


Rendering:

   ====================== ========================= =========================
   Notation               Alt-notation              Result
   ====================== ========================= =========================
   ``:issue:`12345```     ```12345`:issue:``        :issue:`12345`
   ``:forge:`345```       ```345`:forge:``          :forge:`345`
   ``:forge2:`345```      ```345`:forge2:``         :forge2:`345`
   ``:forge3:`345```      ```345`:forge3:``         :forge3:`345`
   ``:forge4:`345```      ```345`:forge4:``         :forge4:`345`
   ``:review:`567```      ```567`:review:``         :review:`567`
   ``:t3ext:`news```      ```news`:t3ext:``         :t3ext:`news`
   ``:t3ext2:`news```     ```news`:t3ext2:``        :t3ext2:`news`
   ``:t3ext3:`news```     ```news`:t3ext3:``        :t3ext3:`news`
   ``:t3ext4:`news```     ```news`:t3ext4:``        :t3ext4:`news`
   ``:packagist:`news```  ```news`:packagist:``     :packagist:`news`
   ``:packagist3:`news``` ```news`:packagist3:``    :packagist3:`news`
   ``:packagist4:`news``` ```news`:packagist4:``    :packagist4:`news`
   ====================== ========================= =========================



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


Other, within page
------------------

Source::

   Let's link to `various`_.

Result:

   Let's link to `various`_.




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


