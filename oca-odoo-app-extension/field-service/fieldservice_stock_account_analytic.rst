===========================================
Field Service - Stock - Analytic Accounting
===========================================

.. 
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! This file is generated by oca-gen-addon-readme !!
   !! changes will be overwritten.                   !!
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! source digest: sha256:a28b5a005d2fe694395043405944b87b9484ae8895e2ab3c17da2a067a52b38a
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

.. |badge1| image:: https://img.shields.io/badge/maturity-Beta-yellow.png
    :target: https://odoo-community.org/page/development-status
    :alt: Beta
.. |badge2| image:: https://img.shields.io/badge/licence-AGPL--3-blue.png
    :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
    :alt: License: AGPL-3
.. |badge3| image:: https://img.shields.io/badge/github-OCA%2Ffield--service-lightgray.png?logo=github
    :target: https://github.com/OCA/field-service/tree/14.0/fieldservice_stock_account_analytic
    :alt: OCA/field-service
.. |badge4| image:: https://img.shields.io/badge/weblate-Translate%20me-F47D42.png
    :target: https://translation.odoo-community.org/projects/field-service-14-0/field-service-14-0-fieldservice_stock_account_analytic
    :alt: Translate me on Weblate
.. |badge5| image:: https://img.shields.io/badge/runboat-Try%20me-875A7B.png
    :target: https://runboat.odoo-community.org/builds?repo=OCA/field-service&target_branch=14.0
    :alt: Try me on Runboat

|badge1| |badge2| |badge3| |badge4| |badge5|

This module allows you to report on the stock output account by analytic account.

It uses the analytic account of the field service location to set the
analytic account on the deliveries.

**Table of contents**

.. contents::
   :local:

Usage
=====

FSM Location
~~~~~~~~~~~~

* Go to Field Service > Master data > Locations
* Create or select a location
* Check that the inventory location is a Customer location
* Go to the Accounting tab
* Set the analytic account

FSM Order
~~~~~~~~~

* Go to Field Service
* Create or select an order
* Select the location
* Go to the Inventory tab to add some products and submit the stock requests

Inventory
~~~~~~~~~

* Go to Inventory > Stock Request Orders > X to process
* Open the stock request order related to your Field Service order
* Set the route on the lines and confirm it
* Process the transfers

Accounting
~~~~~~~~~~

* Go to Accounting > Adviser > Analytic Entries

Known issues / Roadmap
======================

The roadmap of the Field Service application is documented on
`Github <https://github.com/OCA/field-service/issues/1>`_.

Bug Tracker
===========

Bugs are tracked on `GitHub Issues <https://github.com/OCA/field-service/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us to smash it by providing a detailed and welcomed
`feedback <https://github.com/OCA/field-service/issues/new?body=module:%20fieldservice_stock_account_analytic%0Aversion:%2014.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Do not contact contributors directly about support or help with technical issues.

Credits
=======

Authors
~~~~~~~

* Open Source Integrators

Contributors
~~~~~~~~~~~~

* `Open Source Integrators <https://www.opensourceintegrators.com>`_

  * Maxime Chambreuil <mchambreuil@opensourceintegrators.com>

Maintainers
~~~~~~~~~~~

This module is maintained by the OCA.

.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

.. |maintainer-max3903| image:: https://github.com/max3903.png?size=40px
    :target: https://github.com/max3903
    :alt: max3903

Current `maintainer <https://odoo-community.org/page/maintainer-role>`__:

|maintainer-max3903| 

This module is part of the `OCA/field-service <https://github.com/OCA/field-service/tree/14.0/fieldservice_stock_account_analytic>`_ project on GitHub.

You are welcome to contribute. To learn how please visit https://odoo-community.org/page/Contribute.
