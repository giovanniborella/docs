.. _layersearch:


LayerSearch
=============

.. topic:: Overview

    :Dato: 25. aug., 2017
    :Forfatter: **Anders Barfod**

    .. include:: ../_subs/OLDWARNING.rst
    
.. contents:: 
    :depth: 3


Opsætning
#############

LayerSearch aktiveres i konfigurationsfilen som kaldes med parameter i URL.

``http://vidi/app/ballerup/?config=test.json``

Hvilke schemaer, som skal indekseres sættes i https://github.com/ballerupgis/ballerupgis.github.io/blob/master/gc2_config/index_in_es.json

Og så kaldes: ``http://gc2:3000/api/extension/layersearch/index/ballerup``

Bemærk, at Vidi nu kan kan kaldes uden schema i URL'en http://gc2:3000/app/ballerup/[schema]/?config=test.json

Schemaer kan opsættes i config'en. Her i test.json med:

``"schemata": [ "proj_vinterudbud_2016" ]``

`Eksempel på konfigurationsfil <https://github.com/ballerupgis/ballerupgis.github.io/blob/master/gc2_config/test.json>`_
