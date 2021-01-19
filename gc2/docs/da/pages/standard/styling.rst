.. _styling:

#################################################################
Tematisering
#################################################################

.. topic:: Overview

    :Date: |today|
    :GC2-version: 2020.12.0
    :Forfatter: `mapcentia <https://github.com/mapcentia>`_, `giovanniborella <https://github.com/giovanniborella>`_

.. contents:: 
    :depth: 3


*****************************************************************
Tematisering
***************************************************************** 

.. include:: ../../_subs/NOTE_GETTINGSTARTED.rst

Alt data der udstilles igennem GC2 er opdelt i lag. Disse ligger i et skama, som igen ligger i en database. Databasen er oprettet når der oprettes en bruger, derefter kan der oprettes flere skemaer. Subusers kan også have deres eget skema, se mere her :ref:`subuser`.

Der findes flere forskellige lag:
* x 

.. _styling_wizard:

Class Wizard
=================================================================

.. include:: ../../_subs/WARNING_OLD_DOC.rst


For nemt at oprette en tematisering, er der lavet en wizard.

.. figure:: ../../../_media/styling-wizard.png
    :width: 400px
    :align: center
    :name: styling-wizard
    :figclass: align-center

    ``Class wizard`` i ``Map``-fanen


Start med at vælge det lag du gerne vil tematisere. Lagene er samlet i de grupper som er defineret i deres :ref:`layer_properties`.

1. Vælg relevant lag der skal tematiseres.
2. Klik på ``Class Wizard``

Tematiseringen af styres igennem regler kaldet ``class``. Dette svarer til et reglset i MapServer-komponenter, og mange af de samme tematiseringsmuligheder er i GC2.

.. _styling_wizard:

Wizard-typer
-----------------------------------------------------------------

.. include:: ../../_subs/WARNING_OLD_DOC.rst

.. figure:: ../../../_media/styling-wizard-open.png
    :width: 400px
    :align: center
    :name: styling-wizard-open
    :figclass: align-center

    ``Class wizard`` viser altid den sidst brugte opsætning

Man bliver præsenteret for 4 faner med hver sin tematisering. Felterne i (**6**) er tilgængelige for alle 4 faner, hvorimod de obligatoriske felter i (**5**) er forskellige for hver fane.

1.  ``Enkelt`` er den mest simple tematisering. Denne stilart bliver sat når der bliver uploaded ny data. Der bliver lavet en ``class`` med den valgte farve.
    * ``Farve`` - den faste farve som features får.

2. ``Unique`` laver en ``class`` for hver unik værdi i det valgte felt.
    * ``Felt`` - vælg hvilken kolonne værdierne skal læses fra.
    * ``Farve`` - Det er muligt at vælge tilfældige farver, eller en af de forud-defineret farve-paletter.

.. note::
    Bemærk at denne stilart ikke sikrer at nye unikke værdier får deres egen tematisering. Dette er en enten-eller regl. Hvis der kommer features som ikke er defineret som en ``expression``, vil de ikke blive udtegnet.

3. ``Intervaller`` laver en ``class`` for et interval. Denne funktion virker kun på nummeriske kolonner.
    * ``Type`` - Det er muligt at vælge mellem  ``Equal`` el. ``Quantile`` til beregningsmetoden for intervallerne.
    * ``Nummerisk felt`` - Hvilken kolonne skal bruges til beregningen.
    * ``Antal af farver`` - Vælg antal af intervaller der skal beregnes.
    * ``Start Farve`` - Vælg den indledende farve
    * ``Slut Farve`` - Vælg den afsluttende farve

4. ``Clusters`` laver en gruppering af punkter eller features. Det bliver lavet en ``class`` for grupperingen, og den enkelte feature.
    * ``Afstand`` - heltal i ``pixels`` som angiver hvor tæt features skal ligge på hinanden for at indgå i en cluster.

.. _styling_wizard_symbol:

Symbol
-----------------------------------------------------------------

.. include:: ../../_subs/WARNING_OLD_DOC.rst

.. figure:: ../../../_media/styling-wizard-symbol.png
    :width: 400px
    :align: center
    :name: styling-wizard-symbol
    :figclass: align-center

    Indstillinger for ``Symbol``

1. ``Symbol`` - Angiv hvilket symbol der skal bruges. Hvis feltet er tomt bliver flader og linjer udtegnet som normalt. 
2. ``Angle`` - Symbolets rotation i ``°`` mod uret.[#combo]_
3. ``Size`` - Symbolets højde i ``pixels``.[#combo]_
4. ``Outline farve`` - Farve der bruges i kanten af flader, og på bestemte symboler. Har ingen effekt på linje-lag.
5. ``Line width`` - Tykkelse på linjer i ``pixels``
6. ``Gennemsigtighed`` - Angiv gennemsigtighed på objektet på en skala fra ``1 - 100`` hvor ``100`` er solid. 

.. _styling_wizard_label:

Label
-----------------------------------------------------------------

.. include:: ../../_subs/WARNING_OLD_DOC.rst

.. figure:: ../../../_media/styling-wizard-label.png
    :width: 400px
    :align: center
    :name: styling-wizard-label
    :figclass: align-center

    Indstillinger for ``Label``

1. ``Text``
2. ``Color``
3. ``Size``
4. ``Position``
5. ``Angle``
6. ``Background``
7. ``Font``
8. ``Font weight``

.. _styling_manual:

Manuel tematisering
=================================================================

TBD


.. _styling_qgis:

QGIS
=================================================================

Det er også muligt at tematisere alle sine lag på én gang, eller enkeltvis med at uploade et QGIS-projekt som beskrevet her: :ref:`layer_create_qgis`. Tematiseringen vil i vid udstrækning blive overført fra projektet.

.. note::
    Hvis lagene bliver tematiseret gennem QGIS-projekt skal man være opmærksom på at hele projektet skal læses af MapServer inde der kan returneres et svar til klienten. Det betyder at man kan hente et væsentligt performance-boost ved at tematisere sing lag igennem MapServer.


.. rubric:: Footnotes

  .. [#combo] Combobox - Man kan angive en fast værdi, eller koble til en kolonne.