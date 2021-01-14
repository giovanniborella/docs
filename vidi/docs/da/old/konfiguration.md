Den grundlæggende VIDI URL består af følgende:
 "host" /app/  "Databasenavn" /  "schema(kan sættes fra config)" /  "?config=x.json"  #  "baggrundlag"  /  "zoom niveau"  /  "koordinat, koordinat"  /  "aktiverede  tables"

Her ligger konfigurationsfiler, som kan bruges til opsætning af VIDI:
https://github.com/ballerupgis/ballerupgis.github.io/tree/master/gc2_config

URL til at kalde json: 
https://ballerupgis.github.io/gc2_config/konflikt.json

Herfter kan kan opsætningen kaldes med parametren:`?config=konflikt.json` <br>
Ex: http://gc2:3000/app/ballerup/_17_undervisning/?config=konflikt.json <br> 
http://ballerup-vidi.mapcentia.com/app/ballerup/_17_undervisning/?config=konflikt.json

I configgen kan der sættes en basic template som bliver hentet fra Mapcentias Github. Her kan der laves customization af VIDI (https://github.com/mapcentia/vidi/tree/master/public/templates/standard).

Et eksempel på template ændring – Naturpark lillebælt template: https://marsvin.naturparklillebaelt.dk/app/naturparklillebaelt/public/#stamenTonerLite/12/9.6779/55.4869/.