==============
Documentazione
==============

Elenco cartelle:

* documentazione: guide per la documentazione
   gruppo di riferimento https://www.odoo-italia.org/contribuire/documentazione
* sviluppo: guide per sviluppatori
   gruppo di riferimento https://www.odoo-italia.org/contribuire/sviluppo
* test: guide per eseguire test funzionali
   gruppo di riferimento https://www.odoo-italia.org/contribuire/test
* traduzioni: guide per fare traduzioni
   gruppo di riferimento https://www.odoo-italia.org/contribuire/traduzioni
* promozione: guide per la creazione di eventi
   gruppo di riferimento https://www.odoo-italia.org/contribuire/promozione
* web: guide per gestire le pagine del sito web e il forum
   gruppo di riferimento https://www.odoo-italia.org/contribuire/web

* guide: guide utente 
   gruppo di riferimento https://www.odoo-italia.org/contribuire/documentazione

Requisiti per la generazione delle pagine HTML:

* Python 3.5+
* `Sphinx <http://sphinx-doc.org>`_ 1.4.2+ fino alla 1.8.5, consultare `la documentazione sphinx <http://sphinx-doc.org/install.html>`_ per installare in locale.
* werkzeug
* sphinx-patchqueue
* `git <http://www.git-scm.com>`_

Generazione delle documentazione HTML in locale :

* Clonare questo repository:

  .. code-block:: console

     $ git clone https://github.com/odoo-italia/documentazione.git
     
* Eseguire questo comando dentro la cartella ``documentazione``:

  .. code-block:: console

     $ make html

  
Per accedere alla documentazione HTML generata aprire il file ``_build/html/index.html``.
