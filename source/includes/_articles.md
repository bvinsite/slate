## Articles

Articles add additional information to products required in the rest of the Exposit application.

> Example Article

```json
{
   "data":{
      "id":"016b2bc4-df9c-42b0-ac4b-d54f7fcbea8e",
      "type":"articles",
      "links":{
         "self":"https://api.nextposit.nl/api/v31/articles/016b2bc4-df9c-42b0-ac4b-d54f7fcbea8e"
      },
      "attributes":{
         "fixed-base-price":"3022.94",
         "fixed-base-price-with-tax":3295,
         "name":"Smulsteen Mixed Grill Trio",
         "sku":null,
         "plu":"1733",
         "created-at":"2019-02-11T14:03:40.000+01:00",
         "updated-at":"2019-03-19T16:52:01.318+01:00"
      },
      "relationships":{
         "components":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/articles/016b2bc4-df9c-42b0-ac4b-d54f7fcbea8e/relationships/components",
               "related":"https://api.nextposit.nl/api/v31/articles/016b2bc4-df9c-42b0-ac4b-d54f7fcbea8e/components"
            }
         },
         "selections":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/articles/016b2bc4-df9c-42b0-ac4b-d54f7fcbea8e/relationships/selections",
               "related":"https://api.nextposit.nl/api/v31/articles/016b2bc4-df9c-42b0-ac4b-d54f7fcbea8e/selections"
            }
         },
         "tags":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/articles/016b2bc4-df9c-42b0-ac4b-d54f7fcbea8e/relationships/tags",
               "related":"https://api.nextposit.nl/api/v31/articles/016b2bc4-df9c-42b0-ac4b-d54f7fcbea8e/tags"
            }
         },
         "company":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/articles/016b2bc4-df9c-42b0-ac4b-d54f7fcbea8e/relationships/company",
               "related":"https://api.nextposit.nl/api/v31/articles/016b2bc4-df9c-42b0-ac4b-d54f7fcbea8e/company"
            }
         },
         "sales-tax":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/articles/016b2bc4-df9c-42b0-ac4b-d54f7fcbea8e/relationships/sales-tax",
               "related":"https://api.nextposit.nl/api/v31/articles/016b2bc4-df9c-42b0-ac4b-d54f7fcbea8e/sales-tax"
            }
         }
      }
   }
}
```

### Attributes

| Name                        | Format    |  Description        |
| --------------------------- | --------- | ------------------- |
| fixed-base-price            | decimal   |  pre-tax price in cents, overrides calculated price of underlying products
| fixed-base-price-with-tax   | integer   |  tax price in cents
| name                        | string    | *required*
| sku                         | string    |
| plu                         | string    | *required, unique*
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*

### Filters

| Parameter                   | Format    |  Partial Matches    |
| --------------------------- | --------- | ------------------- |
| plu                         | string    |  N
| sku                         | string    |  N
| name                        | string    |  Y
| created_after               | timestamp |  N/A
| updated_after               | timestamp |  N/A

### Relationships

* [Company](#companies)
* [SalesTax](#salestaxes)
* [Components](#components)
* [Selections](#selections)
* [Tags](#tags)
