===============
Google Map View
===============

.. 
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! This file is generated by oca-gen-addon-readme !!
   !! changes will be overwritten.                   !!
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
   !! source digest: sha256:9a53bf4aef9d09814005307b9a3ba76588d68994ec466f879a4d0d0aa4350451
   !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

.. |badge1| image:: https://img.shields.io/badge/maturity-Beta-yellow.png
    :target: https://odoo-community.org/page/development-status
    :alt: Beta
.. |badge2| image:: https://img.shields.io/badge/licence-AGPL--3-blue.png
    :target: http://www.gnu.org/licenses/agpl-3.0-standalone.html
    :alt: License: AGPL-3
.. |badge3| image:: https://img.shields.io/badge/github-OCA%2Fgeospatial-lightgray.png?logo=github
    :target: https://github.com/OCA/geospatial/tree/14.0/web_view_google_map
    :alt: OCA/geospatial
.. |badge4| image:: https://img.shields.io/badge/weblate-Translate%20me-F47D42.png
    :target: https://translation.odoo-community.org/projects/geospatial-14-0/geospatial-14-0-web_view_google_map
    :alt: Translate me on Weblate
.. |badge5| image:: https://img.shields.io/badge/runboat-Try%20me-875A7B.png
    :target: https://runboat.odoo-community.org/builds?repo=OCA/geospatial&target_branch=14.0
    :alt: Try me on Runboat

|badge1| |badge2| |badge3| |badge4| |badge5|

This module contains three new features:
 - New view type and mode `"map"`
 - New widget `"gplaces_address_autocomplete"`
 - New widget `"gplaces_autocomplete"`

**Table of contents**

.. contents::
   :local:

Usage
=====

Map view  `"map"`:-

Basically, this new view `map`  will integrate Google Maps into Odoo.
Enable you to display `res.partner` geolocation on map or any model contains geolocation.
This feature will work seamlessly with Odoo means you can search your partner location using Odoo search feature.

There are five available attributes that you can customize:-

 - `lat` : an attritube to tell the map the latitude field on the object __[mandatory]__
 - `lng` : an attritute to tell the map the longitude field on the object __[mandatory]__
 - `color` : an attribute to modify marker color (optional) any given color will set all markers color __[optional]__.
 - `colors` : work like attribute `color` but more configurable (you can set marker color depends on it's value) this attribute works similar to `colors` of tree view on Odoo __[optional]__
 - `library` : an attribute to tell map which map that will be loaded __[mandatory]__.
    This options has two values:
    1. `geometry`
    2. `drawing`

The XML Map view definitions. For instance::

    <record id="view_res_partner_map" model="ir.ui.view">
        <field name="name">view.res.partner.map</field>
        <field name="model">res.partner</field>
        <field name="arch" type="xml">
            <map class="o_res_partner_map" library='geometry' string="Map" lat="partner_latitude" lng="partner_longitude" colors="blue:company_type=='person';green:company_type=='company';">
                <field name="id"/>
                <field name="partner_latitude"/>
                <field name="partner_longitude"/>
                <field name="company_type"/>
                <field name="color"/>
                <field name="display_name"/>
                <field name="title"/>
                <field name="email"/>
                <field name="parent_id"/>
                <field name="is_company"/>
                <field name="function"/>
                <field name="phone"/>
                <field name="street"/>
                <field name="street2"/>
                <field name="zip"/>
                <field name="city"/>
                <field name="country_id"/>
                <field name="mobile"/>
                <field name="state_id"/>
                <field name="category_id"/>
                <field name="image_small"/>
                <field name="type"/>
                <templates>
                    <t t-name="kanban-box">
                        <div class="oe_kanban_global_click o_res_partner_kanban">
                            <div class="o_kanban_image">
                                <t t-if="record.image_small.raw_value">
                                    <img t-att-src="kanban_image('res.partner', 'image_small', record.id.raw_value)"/>
                                </t>
                                <t t-if="!record.image_small.raw_value">
                                    <t t-if="record.type.raw_value === 'delivery'">
                                        <img t-att-src='_s + "/base/static/src/img/truck.png"' class="o_kanban_image oe_kanban_avatar_smallbox"/>
                                    </t>
                                    <t t-if="record.type.raw_value === 'invoice'">
                                        <img t-att-src='_s + "/base/static/src/img/money.png"' class="o_kanban_image oe_kanban_avatar_smallbox"/>
                                    </t>
                                    <t t-if="record.type.raw_value != 'invoice' &amp;&amp; record.type.raw_value != 'delivery'">
                                        <t t-if="record.is_company.raw_value === true">
                                            <img t-att-src='_s + "/base/static/src/img/company_image.png"'/>
                                        </t>
                                        <t t-if="record.is_company.raw_value === false">
                                            <img t-att-src='_s + "/base/static/src/img/avatar.png"'/>
                                        </t>
                                    </t>
                                </t>
                            </div>
                            <div class="oe_kanban_details">
                                <strong class="o_kanban_record_title oe_partner_heading">
                                    <field name="display_name"/>
                                </strong>
                                <div class="o_kanban_tags_section oe_kanban_partner_categories">
                                    <span class="oe_kanban_list_many2many">
                                        <field name="category_id" widget="many2many_tags" options="{'color_field': 'color'}"/>
                                    </span>
                                </div>
                                <ul>
                                    <li t-if="record.parent_id.raw_value and !record.function.raw_value">
                                        <field name="parent_id"/>
                                    </li>
                                    <li t-if="!record.parent_id.raw_value and record.function.raw_value">
                                        <field name="function"/>
                                    </li>
                                    <li t-if="record.parent_id.raw_value and record.function.raw_value">
                                        <field name="function"/> at <field name="parent_id"/>
                                    </li>
                                    <li t-if="record.city.raw_value and !record.country_id.raw_value">
                                        <field name="city"/>
                                    </li>
                                    <li t-if="!record.city.raw_value and record.country_id.raw_value">
                                        <field name="country_id"/>
                                    </li>
                                    <li t-if="record.city.raw_value and record.country_id.raw_value">
                                        <field name="city"/>
                ,                        <field name="country_id"/>
                                    </li>
                                    <li t-if="record.email.raw_value" class="o_text_overflow">
                                        <field name="email"/>
                                    </li>
                                </ul>
                                <div class="oe_kanban_partner_links"/>
                            </div>
                        </div>
                    </t>
                </templates>
            </map>
        </field>
    </record>

    <record id="action_partner_map" model="ir.actions.act_window">
        ...
        <field name="view_type">form</field>
        <field name="view_mode">tree,form,map</field>
        ...
    </record>

The marker info window will use `kanban-box` kanban card style.

How to setup color for marker on map?

There are two attributes:

 - `colors`: Allow you to display different marker color to represent a record on map

 - `color`: One marker color for all records on map

The XML color view definitions. For instance::

    <!-- colors -->
    <map string="Map" lat="partner_latitude" lng="partner_longitude" colors="green:company_type=='person';blue:company_type=='company';">
        ...
    </map>

    <!-- color -->
    <map string="Map" lat="partner_latitude" lng="partner_longitude" color="orange">
        ...
    </map>

New widget `"gplaces_address_autocomplete"`:-

New widget to integrate [Place Autocomplete Address Form](https://developers.google.com/maps/documentation/javascript/examples/places-autocomplete-addressform) in Odoo.

The widget has four options that can be modify:

 - `component_form`
 - `fillfields`
 - `lat`
 - `lng`

Component form `component_form`:-

Is an option used to modify which value you want to take from an objects returned by the geocoder.
Full documentation about Google component types can be found [here](https://developers.google.com/maps/documentation/geocoding/intro#Types)

By default this option are configured like the following javascript value::

    {
        'street_number': 'long_name',
        'route': 'long_name',
        'intersection': 'short_name',
        'political': 'short_name',
        'country': 'short_name',
        'administrative_area_level_1': 'short_name',
        'administrative_area_level_2': 'short_name',
        'administrative_area_level_3': 'short_name',
        'administrative_area_level_4': 'short_name',
        'administrative_area_level_5': 'short_name',
        'colloquial_area': 'short_name',
        'locality': 'short_name',
        'ward': 'short_name',
        'sublocality_level_1': 'short_name',
        'sublocality_level_2': 'short_name',
        'sublocality_level_3': 'short_name',
        'sublocality_level_5': 'short_name',
        'neighborhood': 'short_name',
        'premise': 'short_name',
        'postal_code': 'short_name',
        'natural_feature': 'short_name',
        'airport': 'short_name',
        'park': 'short_name',
        'point_of_interest': 'long_name'
    }

This configuration can be modify into xml view field definition::

    <record id="view_res_partner_form" model="ir.ui.view">
       ...
       <field name="arch" type="xml">
            ...
            <field name="street" widget="gplaces_address_form" options="{'component_form': {'street_number': 'short_name'}}"/>
            ...
        </field>
    </record>

Fill fields `fillfields`:-

Is an option that will be influenced by `gplaces_address_autocomplete` widget.

This options should contains known `fields` that you want the widget to fulfill a value for each given field automatically.
A field can contains one or multiple elements of component form
By default this options are configured like the following javascript value::

    {
        'street': ['street_number', 'route'],
        'street2': ['administrative_area_level_3', 'administrative_area_level_4', 'administrative_area_level_5'],
        'city': ['locality', 'administrative_area_level_2'],
        'zip': 'postal_code',
        'state_id': 'administrative_area_level_1',
        'country_id': 'country',
    }

This configuration can be modify into xml view field definition as well::

    <record id="view_res_partner_form" model="ir.ui.view">
        ...
        <field name="arch" type="xml">
            ...
            <field name="street" widget="google_places" options="{'fillfields': {'street2': ['route', 'street_number']}}"/>
            ...
        </field>
    </record>

Latitude `lat` and Longitude `lng`:-

This options tell the widget the fields geolocation, in order to have this fields filled automatically.

New widget `"gplaces_autocomplete"`:-

New widget to integrate [Place Autocomplete](https://developers.google.com/maps/documentation/javascript/examples/places-autocomplete) in Odoo.
This widget have similar configuration to `gplaces_address_autocomplete`.

Component form `component_form`:-

Same configuration of `gplaces_address_autocomplete` component form

Fill fields `fillfields`:-

This configuration works similar to `gplaces_address_autocomplete`.
By default this options are configured like following javascript value::

    {
        general: {
            name: 'name',
            website: 'website',
            phone: ['international_phone_number', 'formatted_phone_number']
        },
        geolocation: {
            partner_latitude: 'latitude',
            partner_longitude: 'longitude'
        },
        address: {
            street: ['street_number', 'route'],
            street2: ['administrative_area_level_3', 'administrative_area_level_4', 'administrative_area_level_5'],
            city: ['locality', 'administrative_area_level_2'],
            zip: 'postal_code',
            state_id: 'administrative_area_level_1',
            country_id: 'country'
        }
    };

Bug Tracker
===========

Bugs are tracked on `GitHub Issues <https://github.com/OCA/geospatial/issues>`_.
In case of trouble, please check there if your issue has already been reported.
If you spotted it first, help us to smash it by providing a detailed and welcomed
`feedback <https://github.com/OCA/geospatial/issues/new?body=module:%20web_view_google_map%0Aversion:%2014.0%0A%0A**Steps%20to%20reproduce**%0A-%20...%0A%0A**Current%20behavior**%0A%0A**Expected%20behavior**>`_.

Do not contact contributors directly about support or help with technical issues.

Credits
=======

Authors
~~~~~~~

* Open Source Integrators

Contributors
~~~~~~~~~~~~

* Yopi Angi <yopiangi@gmail.com>
* Wolfgang Hall <whall@opensourceintegrators.com>
* Serpent Consulting Services Pvt. Ltd. <support@serpentcs.com>
* Ammar Officewala <aofficewala@opensourceintegrators.com>

Maintainers
~~~~~~~~~~~

This module is maintained by the OCA.

.. image:: https://odoo-community.org/logo.png
   :alt: Odoo Community Association
   :target: https://odoo-community.org

OCA, or the Odoo Community Association, is a nonprofit organization whose
mission is to support the collaborative development of Odoo features and
promote its widespread use.

.. |maintainer-gityopie| image:: https://github.com/gityopie.png?size=40px
    :target: https://github.com/gityopie
    :alt: gityopie
.. |maintainer-wolfhall| image:: https://github.com/wolfhall.png?size=40px
    :target: https://github.com/wolfhall
    :alt: wolfhall

Current `maintainers <https://odoo-community.org/page/maintainer-role>`__:

|maintainer-gityopie| |maintainer-wolfhall| 

This module is part of the `OCA/geospatial <https://github.com/OCA/geospatial/tree/14.0/web_view_google_map>`_ project on GitHub.

You are welcome to contribute. To learn how please visit https://odoo-community.org/page/Contribute.
