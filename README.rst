==============
Documentazione
==============

Elenco cartelle:

* guide: Guide utente
   gruppo di riferimento https://www.odoo-italia.org/contribuire/documentazione
* sviluppo: Guide per sviluppatori
   gruppo di riferimento https://www.odoo-italia.org/contribuire/sviluppo
* test: Guide per eseguire test funzionali
   gruppo di riferimento https://www.odoo-italia.org/contribuire/test
* traduzioni: Guide per fare traduzioni
   gruppo di riferimento https://www.odoo-italia.org/contribuire/traduzioni
* promozione: Guide per la creazione di eventi
   gruppo di riferimento https://www.odoo-italia.org/contribuire/promozione
* web: Guide per gestire le pagine del sito web e il forum
   gruppo di riferimento https://www.odoo-italia.org/contribuire/web

Requisiti per la generazione delle pagine HTML:

* Python 3.5+
* `Sphinx <http://sphinx-doc.org>`_, vedi `la documentazione sphinx <http://sphinx-doc.org/install.html>`_ per installare in locale.
* `git <http://www.git-scm.com>`_
* Clona questo repository utilizzando git, quindi nella root esegui:

  .. code-block:: console

     $ make html

  questo compilerà la documentazione in HTML, potrai accedere aprendo il file ``_build/html/index.html``.
