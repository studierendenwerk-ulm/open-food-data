___
# Spezifikation der JSON Daten 
___

## [/bsp-json/menu/ ](https://github.com/studierendenwerk-ulm/open-food-data/blob/bsp-realdata/bsp-json/menu/610/2017/by-day/610-2017-12-11.json)

|G = garantierte Werte | O = optionale Werte|
|:-:|:-:|

|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:| 
|`"timestamp"`|*string*|NA|G|`"timestamp": "2017-12-20T16:34:41+01:00"`|Zeitpunkt wann diese JSON genneriert wurde|
|`"specVersion"`|*number*|NA|G|`"specVersion": 0`|hier wird die Version der JSON dargestellt|
|`"shopId"`|*string*|AUSGABENSTELLEID|G|`"shopId": "610"`|-| 
|`"date"`|*string*|PRODUKTIONSDATUM|G|`"date": "2017-12-11"`|-|
|`"closed"`|*boolean/array*|NA|O|`"closed": null`|-|
|`"meals"`|*array*|NA|G |`"meals": [{},{},...,{}]`|Array aus Objekten|

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

|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"mealId"`|*number*|DISPOART_ID|G|`"mealId": 61`|-| 
|`"currentlyAvailable"`|*boolean*|NA|O|`"currentlyAvailable": true`|-|
|`"description"`|*object*|BEZEICHNUNG |G|`"description": {"DE": "Brokkolicremsuppe","EN": null }`|-|
|`"dispositionId"`|*number*|DISPOART_ID|G|`"dispositionId": 61`|-|
|`"dispositionDescription"`|*object*|SPARTENBEZEICHNUNG|G|`"description": {"DE":"Suppe","EN": null }`|-|
|`"recommendedOrdering"`|*number*|ZEILENNUMMER (ZEILENUMMER)?|G|`"recommendedOrdering": 2`|-|
|`"ingredients"`|*array*|ZUSATZKENNZEICHNUNG|G|`"ingredients": ["23","26","34W"]`|-|
|`"characterization"`|*array*|MENUEKENNZEICHNUNG|G|`"characterization": ["van","bio"]`|-|
|`"imgUrlPathSuffix"`|*string/null*|NA|G|`"imgUrlPathSuffix": null`|-|
|`"specialTimeWindow"`|*array*|NA|O|`"specialTimeWindow": [1130,1345]`|-|
|`"price"`|*object*|PREIS1 bis ...5|G|`"price":{"1":1.8,"2":2.25,"3":3.2,"4":5.6}`|-|
|`"nutritionInformation"`|*array/null*|(NÄHRWERTE)?|O|`"nutritionInformation":null`|-|




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

|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"timestamp"`|*string*|NA|G|`"timestamp": "2017-12-20T16:34:41+01:00"`|Zeitpunkt wann diese JSON genneriert wurde|
|`"specVersion"`|*number*|NA|G|`"specVersion": 0`|hier wird die Version der JSON dargestellt|
|`"shopId"`|*string*|AUSGABENSTELLEID|G|`"shopId": "610"`|-|
|`"foodDataUrlPathInfix"`|*string*|-|-|`"foodDataUrlPathInfix": "/menu/610/"`|-|
|`"foodClassificationUrlPathSuffix"`|*string*|-|-|`"foodClassificationUrlPathSuffix": "/shops/classification_default.json"`|-|

|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"priceCategories"`|*object*|-|-|`"priceCategories": {"1": "Studierende","2": "Mitarbeiter","3": "Gäste"}`|-|
|`"1"`|*string*|-|-|`"1": "Studierende"`|-|
|`"2"`|*string*|-|-|`"2": "Mitarbeiter"`|-|
|`"3"`|*string*|-|-|`"3": "Gäste"`|-|


|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"website"`|*string*|-|-|`"website": "https://studierendenwerk-ulm.de/essen-trinken/mensen-und-cafeterien/#einrichtungen-uni-ulm"`|-|
|`"feedback"`|*string*|-|-|`"feedback": "mensa@studierendenwerk-ulm.de"`|-|
|`"specialsPermanent"`|*string*|-|-|`"specialsPermanent": ["Happy Hour von 13:45 bis 14:00 Uhr."]`|-|
|`"importantInformation"`|*string*|-|-|`"importantInformation": "In H3 gab es einen Feueralarm, deshalb musste die Mensa für heute geräumt werden!"`|-|

|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"footNotes"`|*array* ?|-|-|` "footNotes": ["Änderungen vorbehalten.","Wir verwenden jodiertes Salz.","Kontakt: mensa@studierendenwerk-ulm.de"]`|-|


|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"inDoorLocation"`|*object*|-|-|`"inDoorLocation": {"building": "Uni Ost","level": "Niveau 2","room": "Mensa","nextTo": ["Infopoint Studierendenwerk","Gebäudekreuz O25","Eingang Süd"]}`|-|
|`"building"`|*string*|-|-|`"building": "Uni Ost"`|-|
|`"level"`|*string*|-|-|`"level": "Niveau 2"`|-|
|`"room"`|*string*|-|-|`"room": "Mensa"`|-|
|`"nextTo"`|*array*|-|-|`"nextTo": ["Infopoint Studierendenwerk","Gebäudekreuz O25","Eingang Süd"]`|-|




|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"openingHours"`|*array*|-|-|`"openingHours": [{},{},...,{}]`|-|
|`"start"`|*string*|-|-|`"start": "2017-10-16"`|-|
|`"end"`|*string*|-|-|`"end": "2018-02-17"`|-|
|`"periodDescription"`|*string*|-|-|`"periodDescription": "Vorlesungszeit"`|-|
|`"mo"/"di"/...`|*string*|-|-|`"mo": [1130,1400]`|-|


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
      "di": [
        1130,
        1400
      ],
      "mi": [
        1130,
        1400
      ],
      "do": [
        1130,
        1400
      ],
      "fr": [
        1130,
        1330
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
      "di": [
        1130,
        1330
      ],
      "mi": [
        1130,
        1330
      ],
      "do": [
        1130,
        1330
      ],
      "fr": [
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
      "di": [
        1130,
        1400
      ],
      "mi": [
        1130,
        1400
      ],
      "do": [
        1130,
        1400
      ],
      "fr": [
        1130,
        1330
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

|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"characterization"`|*object*|-|-|`"characterization": {"veg": {"description": {"DE": "vegetarisch","EN": "vegetarian"},"recommendedIcon": "img/icons/meatless"}`|-|
|`"veg"`|*object*|-|-|`"veg": {"description": {...}}`|-|
|`"description"`|*object*|-|-|`"description": {"DE": "vegetarisch","EN": "vegetarian"}`|-|
|`"DE"`|*string*|-|-|`"DE": "vegetarisch"`|-|
|`"EN"`|*string*|-|-|`"EN": "vegetarian"`|-|
|` "recommendedIcon"`|*string*|-|-|`"recommendedIcon": "img/icons/meatless"`|-|

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

|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"timestamp"`|*string*|NA|G|`"timestamp": "2017-12-20T16:34:41+01:00"`|Zeitpunkt wann diese JSON genneriert wurde|
|`"spec"`|*string*|NA|G|`"spec": "https://github.com/studierendenwerk-ulm/open-food-data/tree/v0"`|-|
|`"specVersion"`|*number*|-|-|`"specVersion": 0`|-|
|`"company"`|*string*|-|-|`"company": "Studierendenwerk Ulm"`|-|
|`"website"`|*string*|-|-|`"website": "https://studierendenwerk-ulm.de/"`|-|
|`"address"`|*string*|-|-|`"address": "Studierendenwerk Ulm, James-Franck-Ring 8, 89081 Ulm"`|-|
|`"disclaimerData"`|*string*|-|-|`"TODO Nutzungsbedingungen für die hier veröffentlichten Daten: ..., URL"`|-|
|`"shops"`|*array*|-|-|`"shops" : [{},...,{}]`|-|

|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"shopId"`|*string*|-|-|`"shopId": "610"`|-|
|`"name"`|*string*|-|-|`"name": "Mensa, Uni Ulm"`|-|
|`"address"`|*string*|-|-|`"address": "Studierendenwerk Ulm, James-Franck-Ring 8, 89081 Ulm"`|-|
|`"city"`|*array*|-|-|`"city": ["Ulm"]`|-|
|`"universities"`|*array*|-|-|`"universities": ["Uni Ulm","HS Ulm"]`|-|
|`"coordinates"`|*object*|-|-|`"coordinates": {"latitude": 48.422065,"longitude": 9.955517,"altitude": 604}`|-|
|`"latitude"`|*string*|-|-|`"latitude": 48.422065`|-|
|`"longitude"`|*string*|-|-|`"longitude": 9.955517`|-|
|`altitude`|*string*|-|-|`"altitude": 604`|-|
|`"shopMetadataUrlPathSuffix"`|*string*|-|-|`"shopMetadataUrlPathSuffix": "/shops/610.json"`|-|


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

|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`-`|*-*|-|-|`-`|-|
