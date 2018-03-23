# Spezifikation der JSON Daten 
___

## [/bsp-json/menu/ ](https://github.com/studierendenwerk-ulm/open-food-data/blob/bsp-realdata/bsp-json/menu/610/2017/by-day/610-2017-12-11.json)
---
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
---
### einzelne Objekte aus "meals"
|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|-|-|-|-|-|-|
|"mealId"|number|DISPOART_ID|G|"mealId": 61|| 
|"currentlyAvailable"|boolean|NA|O|"currentlyAvailable": true||
|"description"|object|BEZEICHNUNG |||
|"dispositionId"|number||
|"dispositionDescription"||||
|"recommendedOrdering"||||
|"ingredients" ||||
|"characterization"||||
|"imgUrlPathSuffix" ||||
|"specialTimeWindow" ||||
|"price"||||
|"nutritionInformation"||||
|-|-|-|-|-|-|

[Beispiel JSON Mensa ](https://github.com/studierendenwerk-ulm/open-food-data/blob/bsp-realdata/bsp-json/menu/610/2017/by-day/610-2017-12-11.json)
```json
{
  "timestamp": "2017-12-20T16:34:41+01:00",
  "specVersion": 0,
  "shopId": "610",
  "date": "2017-12-11",
  "closed": null,
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
