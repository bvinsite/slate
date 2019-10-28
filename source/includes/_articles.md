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
         "unit-name": null,
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
| fixed-base-price            | decimal   | pre-tax price in cents, overrides calculated price of underlying products
| fixed-base-price-with-tax   | integer   | tax price in cents
| name                        | string    | *required*
| offer-price-ends-at         | timestamp | Offer price valid from
| offer-price-starts-at       | timestamp | Offer price valid until
| offer-price-with-tax        | integer   | Offer price in cents
| plu                         | string    | *required, unique*
| sells-by-weight             | boolean   |
| sku                         | string    |
| unit-name                   | string    |
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*

### Filters

| Parameter                   | Format    |  Partial Matches    |  Allowed values  |
| --------------------------- | --------- | ------------------- | ---------------- |
| plu                         | string    |  N                  |                  |
| sku                         | string    |  N                  |                  |
| name                        | string    |  Y                  |                  |
| created-after               | timestamp |  N/A                |                  |
| updated-after               | timestamp |  N/A                |                  |

### Relationships

* [Company](#companies)
* [SalesTax](#salestaxes)
* [Components](#components)
* [Selections](#selections)
* [Tags](#tags)

### Examples

__Create an article with price including sales_tax__

Assuming SalesTax has a tax percentage 9:

POST an article with an associated tax rate


<div class="center-column"></div>
```
POST /api/v3/articles
```

<div class="center-column"></div>
```json
{
  "data": {
    "type": "articles",
    "attributes": {
      "plu": "1000001",
      "name": "Test Article I",
    },
    "relationships": {
      "sales-tax": {
        "data": {
          "type": "sales-taxes",
          "id": "acc97298-ab78-498f-82f6-73d8e9c803bd"
        }
      }
    }
  }
}
```

PATCH the article with it's price including taxes

<div class="center-column"></div>
```
PATCH /api/v3/articles/d8b55c93-6c08-4a57-a67f-d0a0dc52a288
```
<div class="center-column"></div>
```json
{
  "data": {
    "id": "d8b55c93-6c08-4a57-a67f-d0a0dc52a288",
    "type": "articles",
    "attributes": {
      "fixed-base-price-with-tax": 1090
    }
  }
}
```

Results in the following article

<div class="center-column"></div>
```json
{
  "data": {
    "id": "d95e8ced-f845-48db-be9d-2278c42ff30c",
    ...
    "attributes": {
      "fixed-base-price": "1000.0",
      "fixed-base-price-with-tax": 1090,
      ...
    },
    "relationships": {
      ...
      }
    }
  },
  "meta": {...}
}
```