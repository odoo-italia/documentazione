====================
Linee guida Italiane
====================

Oltre alle `linee guida OCA <https://github.com/OCA/odoo-community.org/blob/master/website/Contribution/CONTRIBUTING.rst>`_, esistono alcune linee guida aggiuntive interne al repository italiano https://github.com/OCA/l10n-italy.

Titolo del modulo
=================

Il titolo del modulo, campo :code:`name`, deve essere composto di due parti unite da '**-**'.

* **ITA**: Prefisso comune a tutti i moduli della localizzazione italiana
* **Nome in italiano**: Titolo del modulo (max. 2/3 parole) con prima lettera maiuscola

Ad esempio: **ITA - Fattura elettronica**

Se il modulo è un'estensione di un modulo base esistente va aggiunta una terza parte (max. 2/3 parole) che indica la funzionalità aggiuntiva.

Ad esempio: **ITA - Fattura elettronica - Emissione**

Riepilogo del modulo
====================

Il riepilogo, campo :code:`summary`, spiega in modo conciso la funzionalità aggiunta dal modulo.

Ad esempio: **Gestione automatica dell'imposta di bollo**

Sito web del modulo
====================

Il sito web del modulo, campo :code:`website`, deve indicare l'indirizzo del repository.

:code:`https://github.com/OCA/l10n-italy`

Descrizione bilingue
====================

Ogni parte descrittiva del README (es. file *DESCRIPTION.rst*, *CONFIGURE.rst*, *USAGE.rst*) deve contenere la spiegazione in italiano e inglese.

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


