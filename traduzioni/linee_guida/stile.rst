Indicazioni linguistiche e stilistiche
======================================

Questa sezione elenca alcuni suggerimenti sullo stile di scrittura da seguire per mantenere coerenti le traduzioni delle applicazioni per lo GNOME Desktop. Verranni presentati anche alcuni errori da non commettere in fase di traduzione.

Questione di stile
------------------

Citando il `manuale di stile per la traduzione`_ della SUN Microsystem,

 ... un buono stile è la migliore garanzia di una comunicazione efficace, permette di ridurre i costi e, in ultima analisi, di migliorare la soddisfazione dei clienti. L’adozione di uno stile che risponda alle esigenze dei lettori comporta minori esigenze di revisione, un numero inferiore di chiamate ai servizi di assistenza e meno esigenze di formazione.

.. _manuale di stile per la traduzione: http://developer.gnome.org/projects/gtp/style-guides/pdf/styleguide-it.pdf

Traduzione letterale
--------------------

Compito del traduttore è di cercare di rimanere il più possibile fedele all'originale: questo non significa necessariamente tradurre letteralmente, bensì cercare di rendere perfettamente quanto esposto del documento originale. Più la traduzione è vicina all'originale, tanto questa è migliore, ma tale vicinanza non deve verificarsi a scapito della forma o della correttezza: a causa del diverso modo di costruire le frasi nelle varie lingue, spesso è da considerare migliore una traduzione che si distacca dall'originale ma è più scorrevole o più elegante.

Tradurre, non spiegare
----------------------

Questa è una massima valida per tutte le traduzioni tecniche. Una traduzione deve cercare di rendere esattamente ciò che è espresso dall'originale, senza sforzarsi di renderlo più chiaro o meno ambiguo, a meno di errori nell'originale che vanno corretti e segnalati agli autori.

Ciò non vuol dire che le traduzioni debbano essere necessariamente letterali (anche se questo può essere comunque considerato un pregio): semplicemente non è compito del traduttore fare precisazioni su un testo ambiguo.

Talvolta ciò può accadere in modo inevitabile per diversità della lingua: ad esempio il termine **free software** in italiano diviene **software libero**. Con una tale traduzione, tuttavia, diviene pressoché impossibile tradurre anche la precisazione che spesso viene fatta tra gli anglofoni: *free as in speech, not as free beer*.

È per evitare casi come questi che il lavoro del traduttore non comprende la chiarificazione di un testo poco chiaro nella sua forma originale: in tali casi il comportamento migliore sarebbe quello di contattare l'autore originale e far presente che il testo contiene delle parti dubbie, sollecitandolo a chiarirle.


Termini stranieri
-----------------

I termini stranieri non vanno mai coniugati al plurale e rimangono sempre nella loro forma singolare: ad esempio si dice *i mouse*, non *i mice*.

Per quanto riguarda il genere, il termine assume quello che avrebbe se tradotto in italiano oppure quello che suona meglio dandogli un significato italiano. In caso di dubbio è consigliabile rifarsi all'uso comune (sempre che ne esista uno) e consultare le risorse messe a disposizione dal `Translation Project italiano`_ (glossario e mailing list).

.. _Translation Project italiano: http://www.linux.it/tp/


Uso di termini stranieri
~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: po

  #: src/dialogs:43
  msgid "Selected %d files, total %d bytes"
  msgstr "Selezionati %d file, in totale %d byte"


Verbi al gerundio
-----------------

Spesso nei testi da tradurre compaiono verbi posti al gerundio (es. *Loading...*) che, se tradotti con un gerundio italiano darebbero un'idea diversa dall'originale.

In questi casi è raccomandabile tradurli sostantivizzando l'azione: *Caricamento...* oppure *Caricamento in corso...* se si volesse porre maggior accento sul contemporaneo svolgimento dell'operazione, anche se ciò appesantisce la frase.

Altre volte è meglio usare il verbo all'infinito per evitare di dover creare nuovi sostantivi o di dover usare forme sostantivizzate poco scorrevoli: usando frasi come *Errore nell'installare il modulo* si riesce, inoltre, a mantenere una certa relazione tra la forma originale e quella tradotta, riducendo la probabilità di dover rigirare la frase.

Italianizzazioni
----------------

Termini stranieri italianizzati (come *settare*, *rebootare*, *pingare*) sono da evitare usando i termini corretti (*impostare*, *riavviare*) o aggirandoli con parafrasi (*effettuare il ping*).

Ovviamente esistono ragionevoli eccezioni a questa regola (ad esempio il termine *zippare*, neologismo anche per la lingua inglese), ma in generale tali italianizzazioni sono spesso da considerare errori linguistici.

Rivolgersi all'utente
---------------------

Mentre i testi inglesi usano solitamente rivolgersi direttamente al destinatario, in italiano è una cosa da evitare, essendo preferibile usare forme impersonali per esprimere gli stessi concetti. La forma impersonale conferisce al programma un tono più professionale o, perlomeno, distaccato.

Ricadono in questa sezione l'uso di domande retoriche, forme interrogative ed esclamative nella documentazione, le forme colloquiali, e l'uso della seconda persona, come verrà evidenziato negli esempi qui di seguito.

È anche opportuno limitare l'uso del *si* impersonale, il quale tende a rendere le frasi pesanti e poco scorrevoli, privilegiando l'uso dell'infinito.

Una possibile eccezione a quanto esposto possono essere i *tour* e alcune parti limitate del *front-end* web.

Si tenga, inoltre, presente che in inglese i programmi tendono a essere incredibilmente educati, anteponendo molti *please* alle azioni che l'utente deve compiere. In italiano, invece, i programmi sono molto più freddi e si limitano a dire all'utente cosa deve fare.

In definitiva, la regola aurea nel tradurre molte delle frasi informative (messaggi di avviso, spiegazioni, sezioni di manuali) è: **leva tutto ciò che non è il messaggio**. Per chiarimenti consultare gli esempi seguenti.

Forme interrogative ed esclamative
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Domande retoriche, frasi esclamative o interrogative e forme colloquiali sono da evitare, cercando di usare al loro posto una forma affermativa impersonale, che conferisce al programma un tono più professionale o, perlomeno, distaccato.

.. code-block:: po

 #: ../panel.xml:502 (title)
 msgid "How do you use an applet?"
 msgstr "Utilizzo delle applet"

 #: ../panel.xml:1024 (para)
 msgid "Let’s get to know the program!"
 msgstr "Nei paragrafi seguenti verrà spiegato il funzionamento del programma."

Forme colloquiali
~~~~~~~~~~~~~~~~~

.. code-block:: po

 #: src/assistant.c:43
 msgid "Now you know what to do if you want to proceed with the installation."
 msgstr "Il processo ora descritto permetterà di procedere con l’installazione."

Forme verbali impersonali e personali
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: po

 #. module: account
 #: model:ir.model.fields,help:account.field_account_invoice__date
 msgid "Keep empty to use the invoice date."
 msgstr "Lasciare vuoto per usare la data fattura."

Tempo futuro e tempo presente
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: po

 #. module: delivery
 #: model:ir.model.fields,help:delivery.field_res_partner__property_delivery_carrier_id
 #: model:ir.model.fields,help:delivery.field_res_users__property_delivery_carrier_id
 msgid "This delivery method will be used when invoicing from picking."
 msgstr "Questo metodo di consegna viene usato nella fatturazione da prelievo."

Verbi modali e imperativo
~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: po

 #. module: mrp
 #: code:addons/mrp/models/mrp_unbuild.py:95
 #, python-format
 msgid "You should provide a lot number for the final product."
 msgstr "Fornire un numero di lotto per il prodotto finale."

Seconda persona singolare e forme impersonali
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: po

 #. module: point_of_sale
 #: model_terms:ir.ui.view,arch_db:point_of_sale.view_pos_open_statement
 msgid "Do you want to open cash registers?"
 msgstr "Aprire i registratori di cassa?"

 #. module: document
 #. openerp-web
 #: code:addons/document/static/src/js/document.js:180
 #, python-format
 msgid "Do you really want to delete this attachment ?"
 msgstr "Eliminare veramente questo allegato?"

 #. module: web
 #. openerp-web
 #: code:addons/web/static/src/js/views/search/favorites_menu.js:273
 #, python-format
 msgid "Are you sure that you want to remove this filter?"
 msgstr "Rimuovere veramente questo filtro?"


Traduzione di *please*
~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: po

 #. module: payment
 #. openerp-web
 #: code:addons/payment/static/src/js/payment_form.js:202
 #, python-format
 msgid "Please select a payment method."
 msgstr "Selezionare un metodo di pagamento."

Personificazione di hardware e software
---------------------------------------

Mentre in inglese il programma si riferisce a se stesso in prima persona, in italiano ciò è da evitare, usando costrutti impersonali o forme passive.

Personificazione dei programmi
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block:: po

 #: src/dialogs:57
 msgid "I'm going to ask you some questions"
 msgstr "Verranno poste alcune domande"

 #: src/dialogs:57
 msgid "The program will delete the document."
 msgstr "Il documento verrà eliminato."

Acronimi
--------

Gli acronimi devono essere utilizzati, ove possibile, nella forma corrente in italiano. Si noti che specialmente per gli acronimi tecnici e per quelli di origine più recente, è invalso l’uso in italiano della forma originale (es. AIDS e non SIDA, ERP e non RPA).

Allo stesso modo è opportuno non usare la forma estesa dell'acronimo quando l'acronimo stesso ha uso più frequente.

.. code-block:: po

 #: data/mimetypes.xml:57
 msgid "eXtensible Markup Language document"
 msgstr "Documento XML (eXtensible Markup Language)"

 #: src/dialogs.c:57
 msgid "Click here to open the URL"
 msgstr "Fare clic qui per aprire l'URL"

Periodi brevi
-------------

Mentre in inglese è diffuso l'uso di brevi periodi in successione legati tra loro, in italiano è considerato un esempio di cattivo stile. Pertanto è consigliabile cercare di fondere questi periodi in periodi più lunghi, articolati in frasi principali e subordinate.

Incisi
------

Nei testi anglofoni è consuetudine inserire incisi introdotti da un trattino **-** o da due trattini **--**: in italiano sono da evitare, sopperendo con l'uso delle virgole o dei due punti.

Disgiunzioni non esclusive
--------------------------

In inglese è frequente incontrare la forma *and/or* per indicare la possibilità che due eventi possano o verificarsi entrambi oppure che se ne verifichi almeno uno dei due, in quanto la disgiunzione *or* ha un significato di mutua esclusione (EXOR).

L'italiano, invece, deriva le proprie congiunzioni e disgiunzioni dal latino, in cui erano presenti:

**et, atque**
  congiunzione (AND logico)
**vel**
  disgiunzione (OR logico)
**aut ... aut ...**
  esclusione (EXOR logico)

Pertanto in italiano la forma *e/o* è da evitare, usando al suo posto una semplice *o*, mentre per esprimere la mutua esclusione è possibile impiegare la forma *o ... o ....*

**you can do this and that**
  è possibile fare questo **e** quello

**you can do this or that**
  è possibile fare **o** questo **o** quello
**you can do this and/or that**
  è possibile fare questo **o** quello
