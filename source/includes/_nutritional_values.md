## NutritionalValues


> Example NutritionalValue

```json
{
    "data": {
        "id": "f71eb9b8-22dc-44c4-b2b7-2bd5951e170a",
        "type": "nutritional-values",
        "links": {
            "self": "http://api.lvh.me:3000/api/v31/nutritional-values/f71eb9b8-22dc-44c4-b2b7-2bd5951e170a"
        },
        "attributes": {
            "kcal": 113,
            "fats": 8,
            "saturated-fats": 4,
            "carbohydrates": 25,
            "sugars": 12,
            "salt": 1,
            "created-at": "2025-01-20T11:05:22.629080+01:00",
            "updated-at": "2025-01-21T11:11:01.818979+01:00"
        },
        "relationships": {
            "product": {
                "links": {
                    "self": "http://api.lvh.me:3000/api/v31/nutritional-values/f71eb9b8-22dc-44c4-b2b7-2bd5951e170a/relationships/product",
                    "related": "http://api.lvh.me:3000/api/v31/nutritional-values/f71eb9b8-22dc-44c4-b2b7-2bd5951e170a/product"
                }
            },
            "company": {
                "links": {
                    "self": "http://api.lvh.me:3000/api/v31/nutritional-values/f71eb9b8-22dc-44c4-b2b7-2bd5951e170a/relationships/company",
                    "related": "http://api.lvh.me:3000/api/v31/nutritional-values/f71eb9b8-22dc-44c4-b2b7-2bd5951e170a/company"
                }
            }
        }
    },
....
}


```

### Attributes

| Name                        | Format    |  Description        |
| --------------------------- | --------- | ------------------- |
| carbohydrates               | integer   |
| fats                        | integer   |
| kcal                        | integer   |
| salt                        | integer   |
| sugars                      | integer   |
| carbohydrates               | integer   |
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*

### Filters

None

### Relationships

* [Company](#customers)
* [Product](#orderlines)

<!-- ### Examples -->
