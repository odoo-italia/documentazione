====================
Linee guida Italiane
====================

Oltre alle `linee guida OCA <https://odoo-community.org/page/module-maturity-levels>`_, esistono alcune linee guida aggiuntive interne al repository italiano https://github.com/OCA/l10n-italy.

Titolo del modulo
=================

Il titolo del modulo deve essere composto di tre parti unite da '**-**':

* **ITA**: Prefisso comune a tutti i moduli della localizzazione italiana
* **Nome in italiano**: Titolo del modulo (2 o 3 parole) con prima lettera maiuscola
* **Funzionalità aggiuntiva**: Eventuale sottotitolo (2 o 3 parole) con prima lettera maiuscola

Ad esempio: **ITA - Fatturazione elettronica - Emissione**


Descrizione bilingue
====================

Ogni parte descrittiva del README (DESCRIPTION.rst, CONFIGURE.rst USAGE.rst) deve avere la spiegazione in italiano e inglese.

Ad esempio:

.. code-block:: rst

  **Italiano**

  Questo modulo consente di generare i file XML della fattura elettronica versione 1.2

  http://www.fatturapa.gov.it/export/fatturazione/it/normativa/f-2.htm

  da inviare al Sistema di Interscambio (SdI).

  http://www.fatturapa.gov.it/export/fatturazione/it/sdi.htm

  **English**

  This module allows you to generate the Electronic Invoice XML files version 1.2

  http://www.fatturapa.gov.it/export/fatturazione/en/normativa/f-2.htm

  to be sent to the Exchange System (ES).

  http://www.fatturapa.gov.it/export/fatturazione/en/sdi.htm


