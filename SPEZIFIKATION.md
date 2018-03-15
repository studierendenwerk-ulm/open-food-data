[![N|Solid](https://studierendenwerk-ulm.de/wp-content/themes/studentenwerk/assets/img/logo.png)](https://nodesource.com/products/nsolid)
## Spezifikation der JSON Daten 



# [/bsp-json/menu/ ](https://github.com/studierendenwerk-ulm/open-food-data/blob/bsp-realdata/bsp-json/menu/610/2017/by-day/610-2017-12-11.json)

| Name | JSON Value | tl1 DB | Beispiel | Hinweis | 
| ---- | ---------- | ------ | -------- |---------|  
| "timestamp"| string | unknown |"timestamp": "2017-12-20T16:34:41+01:00"| hier wird die allgemeine Zeitangabe verwendet|
| "specVersion" | number | unknown | "specVersion": 0 | hier wird die Version der JSON dargestellt|
| "shopId" | string | AUSGABENSTELLEID | "shopId": "610" | 
| "date" | string | PRODUKTIONSDATUM | "date": "2017-12-11"|
| "closed" |    ?     | unknown |  "closed": null |
| "meals" | array | ? | "meals": [{},{},...,{}] | enthaelt objekte von meals
| "mealId" | number | DISPOART_ID | "mealId": 61 | 
| "currentlyAvailable"  | boolean  |   | "currentlyAvailable": true |
|  "description" | object | BEZEICHNUNG | |
| "dispositionId" |number||
| "dispositionDescription" |   |   |   |
| "recommendedOrdering" |   |   |   |
| "ingredients" |   |   |   |
| "characterization" |   |   |   |
| "imgUrlPathSuffix" |   |   |   |
| "specialTimeWindow" |   |   |   |
| "price"  |   |   |   |
| "nutritionInformation"  |   |   |   |
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
