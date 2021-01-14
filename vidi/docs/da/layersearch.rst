.. _layersearch:

##############################################
LayerSearch
##############################################

.. topic:: Overview

    Denne side viser hvordan 

    :Date: 25. Aug. 2017
    :Author: **Anders Barfod**

    .. warning:: Indhold fra denne side er overført direkte fra ældre wiki.

            Indhold kan derfor være uddateret.

            Du er velkommen til at hjælpe med at holde dokumentationen opdateret. Læs mere her `CONTRIBUTING </../CONTRIBUTING.md>`_
    
.. contents:: 
    :depth: 3


Introduktion
#############

LayerSearch aktiveres i konfigurationsfilen som kaldes med parameter i URL.

``http://vidi/app/ballerup/?config=test.json``

Hvilke schemaer, som skal indekseres sættes i https://github.com/ballerupgis/ballerupgis.github.io/blob/master/gc2_config/index_in_es.json

Og så kaldes: ``http://gc2:3000/api/extension/layersearch/index/ballerup``

Bemærk, at Vidi nu kan kan kaldes uden schema i URL'en http://gc2:3000/app/ballerup/[schema]/?config=test.json

Schemaer kan opsættes i config'en. Her i test.json med:

``"schemata": [ "proj_vinterudbud_2016" ]``

Eksempel på konfigurationsfil
