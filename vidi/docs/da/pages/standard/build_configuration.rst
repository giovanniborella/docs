.. _configjs:

#################################################################
Systemkonfiguration
#################################################################

.. topic:: Overview

    :Date: |today|
    :Vidi-version: 2020.11.0
    :Forfatter: **René Borella**

.. contents:: 
    :depth: 3


*****************************************************************
Systemkonfiguration
***************************************************************** 

Vidi kan konfigureres under opstart. Denne konfiguration indehodler information om hvilke extensions der skal indlæses, hvilke print-skabeloner der er tilgængelige med mere.

Laves der en ændring, skal vidi startes igen.

Opbygning
=================================================================

Vidi styres af ``config.js``. Denne fil vil være at finde i ``./vidi/config/``. 

.. _configjs_print:

print
-----------------------------------------------------------------

Denn nøgle indeholder opsætningen af print. Den består af underdele som alle er obligatoriske. Ændringer heri skal 

.. _configjs_print_templates:

templates
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

TBD

For at sikre mulighed for at printe, selv om vidi startes uden opsætning, indsættes følgende for at definere hvilken skabelon der er tilgængelig. Denne liste kan udvides med flere templates som er defineret i :ref:`configjs_print_templates`.

.. code-block:: json

    "enabledPrints": ["print"],

.. _configjs_print_scales:

scales
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

``scales`` er en array af heltal der definérer hvilke zoom-forhold det er muligt at lave print i.

Herunder er et eksempel på en opsætning der kun giver mulighed for print i ``1000``, ``2000`` og ``10000``

.. code-block:: json

    "scales": [1000, 2000, 10000]

.. _configjs_complete_example:

Komplet eksempel
=================================================================

For at se et komplet eksempel på en konfiguration henvises til default config i repo. `Den kan du finde her <https://github.com/mapcentia/vidi/blob/master/config/config.embed.dist.js>`_