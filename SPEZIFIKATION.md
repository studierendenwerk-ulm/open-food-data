___
# Spezifikation der JSON Daten 
___

## [/bsp-json/menu/ ](https://github.com/studierendenwerk-ulm/open-food-data/blob/bsp-realdata/bsp-json/menu/610/2017/by-day/610-2017-12-11.json)

|G = garantierte Werte | O = optionale Werte|
|:-:|:-:|

|Name|JSON Value|DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:| 
|`"timestamp"`|*string*|NA|G|`"timestamp": "2017-12-20T16:34:41+01:00"`|Zeitpunkt wann diese JSON genneriert wurde|
|`"specVersion"`|*number*|NA|G|`"specVersion": 0`|hier wird die Version der JSON dargestellt|
|`"shopId"`|*string*|AUSGABENSTELLEID|G|`"shopId": "610"`|-| 
|`"date"`|*string*|PRODUKTIONSDATUM|G|`"date": "2017-12-11"`|-|
|`"closed"`|*boolean/array*|NA|O|`"closed": null`|wenn null, dann gibt es keine weiteren Informationen, sonst gilt dass es besondere Zeiten gibt, welche in einem Array dargestellt werdfen (siehe [Beispiel JSON SHOPS ](https://github.com/studierendenwerk-ulm/open-food-data/blob/bsp-realdata/bsp-json/shops/610.json) ) |
|`"meals"`|*array*|NA|G |`"meals": [{},{},...,{}]`|ist ein Array aus Objekten, welches wieder Arrays aus Objekten enthalten kann|

[Beispiel JSON Mensa ](https://github.com/studierendenwerk-ulm/open-food-data/blob/bsp-realdata/bsp-json/menu/610/2017/by-day/610-2017-12-11.json)
```json
{
  "timestamp": "2017-12-20T16:34:41+01:00",
  "specVersion": 0,
  "shopId": "610",
  "date": "2017-12-11",
  "closed": null,
  "meals": [{},{},...,{}]
  }
 ````
___

## [einzelne Objekte aus "meals"](https://github.com/studierendenwerk-ulm/open-food-data/blob/bsp-realdata/bsp-json/menu/610/2017/by-day/610-2017-12-11.json)

|G = garantierte Werte | O = optionale Werte|
|:-:|:-:|

|Name|JSON Value|DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"mealId"`|*number*|DISPOART_ID|G|`"mealId": 61`|Jedes Gericht bekommt eine eindeutige ID| 
|`"currentlyAvailable"`|*boolean*|NA|O|`"currentlyAvailable": true`|ist abhängig von der Aktuellen Datenpflege, da es nicht gesichert ist, dass bei einem Ausverkauf auch dieser in dem System registriert wird. Deshalb defoult true|
|`"description"`|*object*|BEZEICHNUNG |G|`"description": {"DE": "Brokkolicremsuppe","EN": null }`|Soll die kurze Bezeichnung des Gerichtes wieder geben in deutch und in englisch (falls vorhanden)|
|`"dispositionId"`|*number*|DISPOART_ID|G|`"dispositionId": 61`|-|
|`"dispositionDescription"`|*object*|SPARTENBEZEICHNUNG|G|`"description": {"DE":"Suppe","EN": null }`|-|
|`"recommendedOrdering"`|*number*|ZEILENNUMMER (ZEILENUMMER)?|G|`"recommendedOrdering": 2`|-|
|`"ingredients"`|*array*|ZUSATZKENNZEICHNUNG|G|`"ingredients": ["23","26","34W"]`|-|
|`"characterization"`|*array*|MENUEKENNZEICHNUNG|G|`"characterization": ["van","bio"]`|hier die gängigen Bezeichungen möglicher Diät-Formen|
|`"imgUrlPathSuffix"`|*string/null*|NA|G|`"imgUrlPathSuffix": null`|Ein Suffix, auch Postfix genannt, ist eine Hinzufügung am Ende eines Wortes. Also die URl plus den genauen Bezeichner|
|`"specialTimeWindow"`|*array*|NA|O|`"specialTimeWindow": [1130,1345]`|-|
|`"price"`|*object*|PREIS1 bis ...5|G|`"price":{"1":1.8,"2":2.25,"3":3.2,"4":5.6}`| vorgesehen sind Studenten, Mitarbeiter, Gäste. Es sollte aber auch eventuell Schüler und eine weiter Option verfügber sein.|
|`"nutritionInformation"`|*array/null*|(NÄHRWERTE)?|O|`"nutritionInformation":null`|hier sollen die Möglichen Nährwerttabellen angeben werden. Wenn dieser Wert null ist, kann keine Information zu diesm Gericht ausgegeb werden.|




[Beispiel JSON Mensa ](https://github.com/studierendenwerk-ulm/open-food-data/blob/bsp-realdata/bsp-json/menu/610/2017/by-day/610-2017-12-11.json)
```json
{
    "meals": [
    {
      "mealId": 61,
      "currentlyAvailable": true,
      "description": {
        "DE": "Brokkolicremsuppe",
        "EN": null
      },
      "dispositionId": 61,
      "dispositionDescription": {
        "DE": "Suppe",
        "EN": null
      },
      "recommendedOrdering": 2,
      "ingredients": [
        "23",
        "26",
        "34W"
      ],
      "characterization": [
        "van",
        "bio"
      ],
      "imgUrlPathSuffix": null,
      "specialTimeWindow": [
        1130,
        1345
      ],
      "price": {
        "1": 1.8,
        "2": 2.25,
        "3": 3.2,
        "4": 5.6
      },
      "nutritionInformation": null
    }
  ]
 }
```
___
## [/bsp-json/shops/ ](https://github.com/studierendenwerk-ulm/open-food-data/blob/bsp-realdata/bsp-json/shops/610.json)
|G = garantierte Werte | O = optionale Werte|
|:-:|:-:|

|Name|JSON Value|DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"timestamp"`|*string*|NA|G|`"timestamp": "2017-12-20T16:34:41+01:00"`|Zeitpunkt wann diese JSON genneriert wurde|
|`"specVersion"`|*number*|NA|G|`"specVersion": 0`|hier wird die Version der JSON dargestellt|
|`"shopId"`|*string*|AUSGABENSTELLEID|G|`"shopId": "610"`|-|
|`"foodDataUrlPathInfix"`|*string*|NA|G|`"foodDataUrlPathInfix": "/menu/610/"`|Ein Infix ist eine Hinzufügung innerhalb eines Wortes. |
|`"foodClassificationUrlPathSuffix"`|*string*|NA|G|`"foodClassificationUrlPathSuffix": "/shops/classification_default.json"`|Ein Suffix, auch Postfix genannt, ist eine Hinzufügung am Ende eines Wortes. |

|Name|JSON Value|DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"priceCategories"`|*object*|PREIS1 bis ...5|G|`"priceCategories": {"1": "Studierende","2": "Mitarbeiter","3": "Gäste"}`|Die priceCategories, sollen eine tendenziell variable Anzahl sein, da es shop abhängig ist, welche Priese genau vorhanden sind. |
|`"1"`|*string*|VKPREIS|G|`"1": "Studierende"`|-|
|`"2"`|*string*|VKPREIS|G|`"2": "Mitarbeiter"`|-|
|`"3"`|*string*|VKPREIS|G|`"3": "Gäste"`|-|


|Name|JSON Value|DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"website"`|*string*|NA|G|`"website": "https://studierendenwerk-ulm.de/essen-trinken/mensen-und-cafeterien/#einrichtungen-uni-ulm"`|-|
|`"feedback"`|*string*|NA|G|`"feedback": "mensa@studierendenwerk-ulm.de"`|-|
|`"specialsPermanent"`|*string*|NA|O|`"specialsPermanent": ["Happy Hour von 13:45 bis 14:00 Uhr."]`|Hier können variable Texter ausgegben werden, um die Kunden über besondere Angebote zu informieren, potenziell kann dies auch ein weiteres meal sein, mit einer eigenen priceCategorie|
|`"importantInformation"`|*string*|NA|O|`"importantInformation": "In H3 gab es einen Feueralarm, deshalb musste die Mensa für heute geräumt werden!"`|Dies sollte sehr Fehlerfrei sein, da so wichtige und lebensnotwendige Informationen herausgegeben werden können, für die nicht gehaftet wird.|

|Name|JSON Value|DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"footNotes"`|*array* ?|NA|G|` "footNotes": ["Änderungen vorbehalten.","Wir verwenden jodiertes Salz.","Kontakt: mensa@studierendenwerk-ulm.de"]`|-|


|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"inDoorLocation"`|*object*|NA|G|`"inDoorLocation": {"building": "Uni Ost","level": "Niveau 2","room": "Mensa","nextTo": ["Infopoint Studierendenwerk","Gebäudekreuz O25","Eingang Süd"]}`|-|
|`"building"`|*string*|NA|G|`"building": "Uni Ost"`|-|
|`"level"`|*string*|NA|G|`"level": "Niveau 2"`|-|
|`"room"`|*string*|NA|G|`"room": "Mensa"`|-|
|`"nextTo"`|*array*|NA|G|`"nextTo": ["Infopoint Studierendenwerk","Gebäudekreuz O25","Eingang Süd"]`|-|




|Name|JSON Value|DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"openingHours"`|*array*|NA|G|`"openingHours": [{},{},...,{}]`|-|
|`"start"`|*string*|NA|G|`"start": "2017-10-16"`|-|
|`"end"`|*string*|NA|G|`"end": "2018-02-17"`|-|
|`"periodDescription"`|*string*|NA|G|`"periodDescription": "Vorlesungszeit"`|-|
|`"mo"/"di"/...`|*string*|NA|G|`"mo": [1130,1400]`|-|


[Beispiel JSON SHOPS ](https://github.com/studierendenwerk-ulm/open-food-data/blob/bsp-realdata/bsp-json/shops/610.json)

````json
{
  "timestamp": "2018-01-25T12:34:41+01:00",
  "specVersion": 0,
  "shopId": "610",
  "foodDataUrlPathInfix": "/menu/610/",
  "foodClassificationUrlPathSuffix": "/shops/classification_default.json",
  "priceCategories": {
    "1": "Studierende",
    "2": "Mitarbeiter",
    "3": "Gäste"
  },
  "website": "https://studierendenwerk-ulm.de/essen-trinken/mensen-und-cafeterien/#einrichtungen-uni-ulm",
  "feedback": "mensa@studierendenwerk-ulm.de",
  "specialsPermanent": [
    "Happy Hour von 13:45 bis 14:00 Uhr."
  ],
  "importantInformation": "In H3 gab es einen Feueralarm, deshalb musste die Mensa für heute geräumt werden!",
  "footNotes": [
    "Änderungen vorbehalten.",
    "Wir verwenden jodiertes Salz.",
    "Kontakt: mensa@studierendenwerk-ulm.de"
  ],
  "inDoorLocation": {
    "building": "Uni Ost",
    "level": "Niveau 2",
    "room": "Mensa",
    "nextTo": [
      "Infopoint Studierendenwerk",
      "Gebäudekreuz O25",
      "Eingang Süd"
    ]
  },
  "openingHours": [
    {
      "start": "2017-10-16",
      "end": "2018-02-17",
      "periodDescription": "Vorlesungszeit",
      "mo": [
        1130,
        1400
      ],
      "sa": null,
      "so": null
    },
    {
      "start": "2018-02-18",
      "end": "2018-04-15",
      "periodDescription": "Vorlesungsfreie Zeit",
      "mo": [
        1130,
        1330
      ],
      "sa": null,
      "so": null
    },
    {
      "start": "2018-04-16",
      "end": "2018-07-21",
      "periodDescription": "Vorlesungszeit",
      "mo": [
        1130,
        1400
      ],
      "sa": null,
      "so": null
    }
  ]
}
````

___
## [/bsp-json/shops/classification_default.json](https://github.com/studierendenwerk-ulm/open-food-data/blob/bsp-realdata/bsp-json/menu/610/2017/by-day/610-2017-12-11.json)
|G = garantierte Werte | O = optionale Werte|
|:-:|:-:|

|Name|JSON Value|DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"characterization"`|*object*|MENUEKENNZTEXT|G|`"characterization": {"veg": {"description": {"DE": "vegetarisch","EN": "vegetarian"},"recommendedIcon": "img/icons/meatless"}`|-|
|`"veg"`|*object*|MENUEKENNZTEXT|G|`"veg": {"description": {...}}`|-|
|`"description"`|*object*|NA|G|`"description": {"DE": "vegetarisch","EN": "vegetarian"}`|-|
|`"DE"`|*string*|MENUEKENNZTEXT|G|`"DE": "vegetarisch"`|-|
|`"EN"`|*string*|NA|O|`"EN": "vegetarian"`|-|
|` "recommendedIcon"`|*string*|NA|O|`"recommendedIcon": "img/icons/meatless"`|-|

[Beispiel JSON classification_defoult](https://github.com/studierendenwerk-ulm/open-food-data/blob/bsp-realdata/bsp-json/shops/classification_default.json)

```json
{
  "characterization": {
    "veg": {
      "description": {
        "DE": "vegetarisch",
        "EN": "vegetarian"
      },
      "recommendedIcon": "img/icons/meatless"
    },
}
```
___
## [/open-food-data/bsp-json/shops.json](https://github.com/studierendenwerk-ulm/open-food-data/blob/bsp-realdata/bsp-json/menu/610/2017/by-day/610-2017-12-11.json)

|Name|JSON Value|DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"timestamp"`|*string*|NA|G|`"timestamp": "2017-12-20T16:34:41+01:00"`|Zeitpunkt wann diese JSON genneriert wurde|
|`"spec"`|*string*|NA|G|`"spec": "https://github.com/studierendenwerk-ulm/open-food-data/tree/v0"`|-|
|`"specVersion"`|*number*|NA|G|`"specVersion": 0`|-|
|`"company"`|*string*|NA|G|`"company": "Studierendenwerk Ulm"`|-|
|`"website"`|*string*|NA|G|`"website": "https://studierendenwerk-ulm.de/"`|-|
|`"address"`|*string*|NA|G|`"address": "Studierendenwerk Ulm, James-Franck-Ring 8, 89081 Ulm"`|-|
|`"disclaimerData"`|*string*|NA|G|`"TODO Nutzungsbedingungen für die hier veröffentlichten Daten: ..., URL"`|-|
|`"shops"`|*array*|NA|G|`"shops" : [{},...,{}]`|-|

|Name|JSON Value|DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"shopId"`|*string*|AUSGABENSTELLENID|G|`"shopId": "610"`|-|
|`"name"`|*string*|NA|G|`"name": "Mensa, Uni Ulm"`|-|
|`"address"`|*string*|NA|G|`"address": "Studierendenwerk Ulm, James-Franck-Ring 8, 89081 Ulm"`|-|
|`"city"`|*array*|NA|G|`"city": ["Ulm"]`|-|
|`"universities"`|*array*|NA|G|`"universities": ["Uni Ulm","HS Ulm"]`|-|
|`"coordinates"`|*object*|NA|G|`"coordinates": {"latitude": 48.422065,"longitude": 9.955517,"altitude": 604}`|-|
|`"latitude"`|*string*|NA|G|`"latitude": 48.422065`|-|
|`"longitude"`|*string*|NA|G|`"longitude": 9.955517`|-|
|`altitude`|*string*|NA|G|`"altitude": 604`|-|
|`"shopMetadataUrlPathSuffix"`|*string*|NA|G|`"shopMetadataUrlPathSuffix": "/shops/610.json"`|-|


```json
{
  "timestamp": "2017-12-20T16:34:41+01:00",
  "spec": "https://github.com/studierendenwerk-ulm/open-food-data/tree/v0",
  "specVersion": 0,
  "company": "Studierendenwerk Ulm",
  "website": "https://studierendenwerk-ulm.de/",
  "address": "Studierendenwerk Ulm, James-Franck-Ring 8, 89081 Ulm",
  "disclaimerData": "TODO Nutzungsbedingungen für die hier veröffentlichten Daten: ..., URL",
  "shops": [
    {
      "shopId": "610",
      "name": "Mensa, Uni Ulm",
      "address": "Studierendenwerk Ulm, James-Franck-Ring 8, 89081 Ulm",
      "city": [
        "Ulm"
      ],
      "universities": [
        "Uni Ulm",
        "HS Ulm"
      ],
      "coordinates": {
        "latitude": 48.422065,
        "longitude": 9.955517,
        "altitude": 604
      },
      "shopMetadataUrlPathSuffix": "/shops/610.json"
    },
    {
      "shopId": "710a",
      "name": "Cafeteria South Side, Uni Ulm",
      "TODO" : "TODO"
    },
    {
      "shopId": "710b",
      "name": "Cafeteria Nord, Uni Ulm",
      "TODO" : "TODO"
    }
]
}
``` 
___
|Name|JSON Value|DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`-`|*-*|-|-|`-`|-|
