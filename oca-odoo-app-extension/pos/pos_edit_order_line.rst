===================
POS Edit Order Line
===================

.. 
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! This file is generated by oca-gen-addon-readme !!
   !! changes will be overwritten.                   !!
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! source digest: sha256:03e0d43c1c0d7fd9ff5874461ffbc809cf0bf22e76c6c0ee2493f9552bd492f8
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

.. |badge1| image:: https://img.shields.io/badge/maturity-Beta-yellow.png
    :target: https://odoo-community.org/page/development-status
    :alt: Beta
.. |badge2| image:: https://img.shields.io/badge/licence-LGPL--3-blue.png
    :target: http://www.gnu.org/licenses/lgpl-3.0-standalone.html
    :alt: License: LGPL-3
.. |badge3| image:: https://img.shields.io/badge/github-OCA%2Fpos-lightgray.png?logo=github
    :target: https://github.com/OCA/pos/tree/14.0/pos_edit_order_line
    :alt: OCA/pos
.. |badge4| image:: https://img.shields.io/badge/weblate-Translate%20me-F47D42.png
    :target: https://translation.odoo-community.org/projects/pos-14-0/pos-14-0-pos_edit_order_line
    :alt: Translate me on Weblate
.. |badge5| image:: https://img.shields.io/badge/runboat-Try%20me-875A7B.png
    :target: https://runboat.odoo-community.org/builds?repo=OCA/pos&target_branch=14.0
    :alt: Try me on Runboat

|badge1| |badge2| |badge3| |badge4| |badge5|

This module adds a button "Edit order lines" in main POS interface to allow an easier UX for cashier when editing product price, qty and discount.

On button click, a popup with order lines allows user to input a clear value for each field, instead of having to use the default process of selecting which field to edit, which is not very intuitive and error-prone.

.. image:: https://raw.githubusercontent.com/OCA/pos/14.0/pos_edit_order_line/static/description/pos_edit_order_line.png
  :alt: Display Edit Order Line Popup

**Table of contents**

.. contents::
   :local:

Configuration
=============

Select PoS > configuration > enable flag "Allow Edit Order Line"
To improve usability when there are more than 3 order lines, we suggest activating the "Large scrollbars" POS setting.

Changelog
=========

14.0.1.0.0
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

* Initial release

Bug Tracker
===========

Bugs are tracked on `GitHub Issues <https://github.com/OCA/pos/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us to smash it by providing a detailed and welcomed
`feedback <https://github.com/OCA/pos/issues/new?body=module:%20pos_edit_order_line%0Aversion:%2014.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Do not contact contributors directly about support or help with technical issues.

Credits
=======

Authors
~~~~~~~

* Ooops
* Cetmix

Contributors
~~~~~~~~~~~~

* Ooops404 <https://www.ooops404.com/>
* Cetmix <https://cetmix.com/>

Maintainers
~~~~~~~~~~~

This module is maintained by the OCA.

.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

This module is part of the `OCA/pos <https://github.com/OCA/pos/tree/14.0/pos_edit_order_line>`_ project on GitHub.

You are welcome to contribute. To learn how please visit https://odoo-community.org/page/Contribute.
