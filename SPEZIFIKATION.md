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
|`"1"`|*-*|-|-|`"1": "Studierende"`|-|
|`"2"`|*-*|-|-|`"2": "Mitarbeiter"`|-|
|`"3"`|*-*|-|-|`"3": "Gäste"`|-|


|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"website"`|*string*|-|-|`"website": "https://studierendenwerk-ulm.de/essen-trinken/mensen-und-cafeterien/#einrichtungen-uni-ulm"`|-|
|`"feedback"`|*string*|-|-|`"feedback": "mensa@studierendenwerk-ulm.de"`|-|
|`"specialsPermanent"`|*string*|-|-|`"specialsPermanent": ["Happy Hour von 13:45 bis 14:00 Uhr."]`|-|
|`"importantInformation"`|*string*|-|-|`"importantInformation": "In H3 gab es einen Feueralarm, deshalb musste die Mensa für heute geräumt werden!"`|-|

|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"footNotes"`|*array* ?|-|-|` "footNotes": ["Änderungen vorbehalten.","Wir verwenden jodiertes Salz.","Kontakt: mensa@studierendenwerk-ulm.de"]`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|

|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"inDoorLocation"`|*object*|-|-|`"inDoorLocation": {"building": "Uni Ost","level": "Niveau 2","room": "Mensa","nextTo": ["Infopoint Studierendenwerk","Gebäudekreuz O25","Eingang Süd"]}`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|



|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"openingHours"`|*array*|-|-|`"openingHours": [{},{},...,{}]`|-|
|`"start"`|*-*|-|-|`"start": "2017-10-16"`|-|
|`"end"`|*-*|-|-|`"end": "2018-02-17"`|-|
|`"periodDescription"`|*-*|-|-|`"periodDescription": "Vorlesungszeit"`|-|
|`"mo"`|*-*|-|-|`"mo": [1130,1400]`|-|
|`-`|*-*|-|-|`-`|-|

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
|`"characterization"`|*-*|-|-|`"characterization": {"veg": {"description": {"DE": "vegetarisch","EN": "vegetarian"},"recommendedIcon": "img/icons/meatless"}`|-|

|"characterization"|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`"veg"`|*-*|-|-|`"veg": {"description": {}}`|-|
|`"description"`|*-*|-|-|`"description": {"DE": "vegetarisch","EN": "vegetarian"}`|-|
|`"DE"`|*-*|-|-|`"DE": "vegetarisch"`|-|
|`"EN"`|*-*|-|-|`"EN": "vegetarian"`|-|

|Name|JSON Value|tl1 DB|G/O|Beispiel|Hinweis| 
|:-:|:-:|:-:|:-:|:-:|:-:|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
|`-`|*-*|-|-|`-`|-|
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
    "kon": {
      "description": {
        "DE": "konventionell",
        "EN": "conventional"
      },
      "iconUrlPathSufix": null
    },
    "bio": {
      "description": {
        "DE": "bio",
        "EN": "bio"
      },
      "recommendedIcon": null
    },
    "van": {
      "description": {
        "DE": "vegan",
        "EN": "vegan"
      },
      "recommendedIcon": "/img/icons/vegan"
    }
  },
  "ingredients": {
    "1": {
      "description": {
        "DE": "Farbstoff",
        "EN": "colouring"
      },
      "recommendedIcon": null
    },
    "2": {
      "description": {
        "DE": "Konservierungsstoff",
        "EN": "preservatives"
      },
      "recommendedIcon": null
    },
    "3": {
      "description": {
        "DE": "Antioxidationsmittel",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "4": {
      "description": {
        "DE": "Geschmacksverstärker",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "5": {
      "description": {
        "DE": "geschwefelt",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "6": {
      "description": {
        "DE": "geschwärzt",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "7": {
      "description": {
        "DE": "gewachst",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "8": {
      "description": {
        "DE": "Phosphat",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "9": {
      "description": {
        "DE": "Süßungsmittel",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "10": {
      "description": {
        "DE": "Phenylalaninquelle",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "11": {
      "description": {
        "DE": "Alkohol",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "13": {
      "description": {
        "DE": "Krebstiere",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "14": {
      "description": {
        "DE": "Eier",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "18": {
      "description": {
        "DE": "Gelatine vom Schwein",
        "EN": ""
      },
      "recommendedIcon": "/img/icons/pork"
    },
    "22": {
      "description": {
        "DE": "Erdnüsse",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "23": {
      "description": {
        "DE": "Soja",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "24": {
      "description": {
        "DE": "Milch/Milchprodukte (mit Laktose)",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "25": {
      "description": {
        "DE": "Schalenfrüchte",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "26": {
      "description": {
        "DE": "Sellerie",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "27": {
      "description": {
        "DE": "Senf",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "28": {
      "description": {
        "DE": "Sesamsamen",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "29": {
      "description": {
        "DE": "Schwefeldioxid",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "30": {
      "description": {
        "DE": "Sulfite",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "31": {
      "description": {
        "DE": "Lupinen",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "32": {
      "description": {
        "DE": "Weichtiere",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "34": {
      "description": {
        "DE": "Gluten",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "35": {
      "description": {
        "DE": "Fisch",
        "EN": ""
      },
      "recommendedIcon": "/img/icons/fish"
    },
    "18R": {
      "description": {
        "DE": "Rindergelatine",
        "EN": ""
      },
      "recommendedIcon": "/img/icons/beef"
    },
    "25C": {
      "description": {
        "DE": "Schalenfrüchte-Cashewkerne",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "25H": {
      "description": {
        "DE": "Schalenfrüchte-Haselnuss",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "25Ma": {
      "description": {
        "DE": "Schalenfrüchte-Macadamia",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "25Mn": {
      "description": {
        "DE": "Schalenfrüchte-Mandel",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "25P": {
      "description": {
        "DE": "Schalenfrüchte-Pistazie",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "25PK": {
      "description": {
        "DE": "Schalenfrüchte-Pekanuss",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "25W": {
      "description": {
        "DE": "schalenfruechte_walnuss",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "34D": {
      "description": {
        "DE": "Gluten-Dinkel",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "34G": {
      "description": {
        "DE": "Gluten-Gerste",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "34H": {
      "description": {
        "DE": "Gluten-Hafer",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "34R": {
      "description": {
        "DE": "Gluten-Roggen",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "34W": {
      "description": {
        "DE": "Gluten-Weizen",
        "EN": ""
      },
      "recommendedIcon": null
    },
    "G": {
      "description": {
        "DE": "Geflügel",
        "EN": ""
      },
      "recommendedIcon": "/img/icons/poultry"
    },
    "L": {
      "description": {
        "DE": "Lamm",
        "EN": ""
      },
      "recommendedIcon": "/img/icons/lamb"
    },
    "R": {
      "description": {
        "DE": "Rind",
        "EN": ""
      },
      "recommendedIcon": "/img/icons/beef"
    },
    "S": {
      "description": {
        "DE": "Schweinefleisch",
        "EN": ""
      },
      "recommendedIcon": "/img/icons/pork"
    }
  }
}
```
