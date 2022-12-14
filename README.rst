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
* `Sphinx <http://sphinx-doc.org>`_ >= 1.4.2 <= 1.8.5
* sphinx-patchqueue
* jinja2 <= 2.11.3
* markupsafe <= 1.1.1
* werkzeug <= 2.1.2
* `git <http://www.git-scm.com>`_

Generazione delle documentazione HTML in locale :

* Clonare questo repository:

  .. code-block:: console

     $ git clone https://github.com/odoo-italia/documentazione.git

* Creare l'ambiente ``virtualenv`` e attivarlo:

  .. code-block:: console

     $ virtualenv -p python3 venv
     $ source venv/bin/activate

* Dentro la cartella ``documentazione`` eseguire i seguenti comandi:

  .. code-block:: console

     $ pip install -r requirements.txt
     $ make html


Per accedere alla documentazione HTML generata aprire il file ``_build/html/index.html``.
