TODO:

LARS: 
[X] link fra kort til DN

DOC: Generelt GC2 (admin) + konvertering fra qgis – består af:
[X] Oprettelse af subuser
[X] Rettighedsstyring
[X] Oprettelse af lag
[X] Håndtering af billeder
[X] Tematisering
[ ] Indlæsning:
    [ ] CAD -> GC2
    [ ] PDF -> Georef PDF (qgis) -> GC2
    [X] Indlæsning af dronefoto, lag
[X] PR to latest release on Mapcentia/GC2
    
DOC: Generelt Vidi (kortmodul) – består af:
[X] Tegneværktøjer
[X] Måleværktøjer
[X] Projekter
[X] printværktøj
[X] PR to latest release on Mapcentia/Vidi

DOC: Specifikt Rønne havn – består af:
[X] Opstart m. login mv.
[X] Oprettelse af komponent
[X] Flytning/Editering af komponenter
[X] Logik ifht. tjek-interval
[X] Håndtering af engangs-job / akut-tjekliste


Til intern
[X] Info
[X] Lagstyring u. filter
[ ] baggrundskort
[ ] Session

GP
[ ] matrikeludpegning
[ ] konfliktanalyse



Scratchpad:

https://mapcentia.screenstepslive.com/s/21003/m/83819


Rst heading marks are currently hard-coded and unchangeable.

    H1: =, H2: -, H3: ^, H4: ~, H5: ", H6: #


################################################################# with overline, for parts
***************************************************************** with overline, for chapters
================================================================= for sections
----------------------------------------------------------------- for subsections
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ for subsubsections
""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""" for paragraphs

.. figure:: ../../../_media/meow.jpg
    :width: 400px
    :align: center
    :alt: meow
    :figclass: align-center
    :name: cat

    figure are like images but with a caption
	

Brug: 900x600 
https://kort.geofyn.dk/app/geofyn/?config=borgerkort01.json#geodk.bright/6/10.47/56.072/


bugs to check:
draw: style: ende: pilehoved, start skal roteres 180gr
draw: reklangel typo "klik og træk for et tegne rektangel" -> "klik og træk for at tegne et rektangel"
draw: cirkelmarker -> annotation?
draw: type translate?

print: oversættelse - landscape/portrait

project: tilgængelig i andre schema, men uden draw?

layers: Signatur for alle lag i subgroup vises under det enkelte lag? se: https://mapgovidi.geopartner.dk/app/geosag/gc2_io_dk_plandatadk/#geodk.bright/16/12.199/55.3075/gc2_io_dk_plandatadk.pdk_kommuneplantillaeg_vedtaget_v


