.. _print:

#################################################################
Print
#################################################################

.. topic:: Overview

    :Date: |today|
    :Forfatter: **René Borella**

.. note:: 
    Indhold i dette værktøj er betinget af opsætningen af Vidi.

.. contents:: 
    :depth: 3


*****************************************************************
Printværktøj
***************************************************************** 

Hvis du er i tvivl om de forskellige UI-elementer, kan du se mere her: :any:`gettingstarted`

Når værktøjet vælges er det indledningsvis slukket.

.. figure:: ../../../_media/print-off.png
    :width: 400px
    :align: center
    :name: print-off
    :figclass: align-center

    Start værktøjet ved klikke på ``Aktivér printværktøjer``

Print
=================================================================

Når værktøjet er tændt er det muligt at tegne elementer ind på kortet. Elementerne er bundet op på den geografiske placering, så de vil blive selv om man panorerer i kortet.

.. figure:: ../../../_media/print-on.png
    :width: 400px
    :align: center
    :name: print-on
    :figclass: align-center

    Værktøjet er tændt, og klar til at printe

Skala
-----------------------------------------------------------------

.. note::
    Dette kan ændres i konfigurationen. Se mere i afsnittet :ref:`scales`

TBD

*****************************************************************
Konfiguration
*****************************************************************

Print-værktøjet kan konfigureres i ``config.js``. Herunder er et eksempel på den del der berører værktøjet.

.. code-block:: json


    ...


    // ===============================================================
    // Configuration of print templates.
    // Print templates must be enabled - look further down.
    // mapsizePx ~ is the pixel dimension of the map view
    // mapsizeMm ~ is actual size of the map view on the resulting PDF
    // ===============================================================

    "print": {
        "templates": {


            // ================================
            // The "print" template is build-in
            // ================================

            "print": {
                A4: {
                    l: {
                        mapsizePx: [1060, 730],
                        mapsizeMm: [280, 192]
                    },
                    p: {
                        mapsizePx: [730, 1060],
                        mapsizeMm: [192, 280]
                    }
                },
                A3: {
                    l: {
                        mapsizePx: [1525, 1065],
                        mapsizeMm: [401, 282]
                    },
                    p: {
                        mapsizePx: [1065, 1525],
                        mapsizeMm: [282, 401]
                    }
                },
                A2: {
                    l: {
                        mapsizePx: [2185, 1525],
                        mapsizeMm: [576, 400]
                    },
                    p: {
                        mapsizePx: [1525, 2185],
                        mapsizeMm: [400, 576]
                    }
                },
                A1: {
                    l: {
                        mapsizePx: [3120, 2185],
                        mapsizeMm: [820, 576]
                    },
                    p: {
                        mapsizePx: [2185, 3120],
                        mapsizeMm: [576, 820]
                    }
                },
                A0: {
                    l: {
                        mapsizePx: [4430, 3120],
                        mapsizeMm: [1173, 825]
                    },
                    p: {
                        mapsizePx: [3120, 4430],
                        mapsizeMm: [825, 1173]
                    }
                }
            },
            "mytemplate": { // Your print templates. "print" is the default
                A4: {
                    l: {
                        mapsizePx: [1060, 730],
                        mapsizeMm: [280, 192]
                    },
                    p: {
                        mapsizePx: [730, 1060],
                        mapsizeMm: [192, 280]
                    }
                }
            },

            // ========================================================
            // Names starting with "_" will not appear in the Print tab
            // But can be used by other extensions.
            // Must not be enabled.
            // ========================================================

            "_conflictPrint": {
                "A4": {
                    "p": {
                        "mapsizePx": [700, 500],
                        "mapsizeMm": [190, 120]
                    }
                }
            }
        },


        // =====================
        // Pre-configured scales
        // =====================

        "scales": [100, 250, 500, 1000, 2000, 3000, 4000, 5000, 7500, 10000, 15000, 25000, 50000, 100000]
    },

    ...

print
=================================================================

Dette element indeholder underliggende indstillinger

templates
-----------------------------------------------------------------

TBD

scales
-----------------------------------------------------------------

``scales`` er en array af heltal der definérer hvilke zoom-forhold det er muligt at lave print i.

Herunder er et eksempel på en opsætning der kun giver mulighed for print i ``1000``, ``2000`` og ``10000``

.. code-block:: json

    "scales": [1000, 2000, 10000]