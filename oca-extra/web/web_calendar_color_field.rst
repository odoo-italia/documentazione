====================
Calendar Color Field
====================

.. 
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! This file is generated by oca-gen-addon-readme !!
   !! changes will be overwritten.                   !!
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! source digest: sha256:82ead62cf29b83b1b91970f62c8924ce76c0253514de9ff207021d65b68baa55
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

.. |badge1| image:: https://img.shields.io/badge/maturity-Beta-yellow.png
    :target: https://odoo-community.org/page/development-status
    :alt: Beta
.. |badge2| image:: https://img.shields.io/badge/licence-AGPL--3-blue.png
    :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
    :alt: License: AGPL-3
.. |badge3| image:: https://img.shields.io/badge/github-OCA%2Fweb-lightgray.png?logo=github
    :target: https://github.com/OCA/web/tree/14.0/web_calendar_color_field
    :alt: OCA/web
.. |badge4| image:: https://img.shields.io/badge/weblate-Translate%20me-F47D42.png
    :target: https://translation.odoo-community.org/projects/web-14-0/web-14-0-web_calendar_color_field
    :alt: Translate me on Weblate
.. |badge5| image:: https://img.shields.io/badge/runboat-Try%20me-875A7B.png
    :target: https://runboat.odoo-community.org/builds?repo=OCA/web&target_branch=14.0
    :alt: Try me on Runboat

|badge1| |badge2| |badge3| |badge4| |badge5|

This is a technical module. It doesn't do anything on its own.

Odoo introduced a mechanism to set the desired color for a calendar filter,
through the field's `color` attribute.

Unfortunately, this only works for filters, but not if we want to use the
calendar's `color` attribute.

This module makes the appropiate changes so that the filter's color is used, if available.

**Table of contents**

.. contents::
   :local:

Usage
=====

Set a color attribute value on any many2one calendar field set as filter and
set the calendar's color attribute to use the same many2one field.

Example:

.. code-block:: xml

    <calendar color="category_id">
        <field name="category_id" filter="1" color="kanban_color"/>
    </calendar>

- `category_id` is a `Many2one` field in your record.
- `kanban_color` is an integer field in your category record.

Bug Tracker
===========

Bugs are tracked on `GitHub Issues <https://github.com/OCA/web/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us to smash it by providing a detailed and welcomed
`feedback <https://github.com/OCA/web/issues/new?body=module:%20web_calendar_color_field%0Aversion:%2014.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Do not contact contributors directly about support or help with technical issues.

Credits
=======

Authors
~~~~~~~

* Iván Todorovich

Contributors
~~~~~~~~~~~~

* Iván Todorovich <ivan.todorovich@gmail.com>

Maintainers
~~~~~~~~~~~

This module is maintained by the OCA.

.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

This module is part of the `OCA/web <https://github.com/OCA/web/tree/14.0/web_calendar_color_field>`_ project on GitHub.

You are welcome to contribute. To learn how please visit https://odoo-community.org/page/Contribute.
