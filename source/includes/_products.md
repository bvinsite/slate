## Products



> Example Product

```json
{
   "data":{
      "id":"00f3b8cd-a0fa-4ba2-a95a-3d3799957c6c",
      "type":"products",
      "links":{
         "self":"https://api.nextposit.nl/api/v31/products/00f3b8cd-a0fa-4ba2-a95a-3d3799957c6c"
      },
      "attributes":{
         "description":null,
         "name":"Megaburgers",
         "plu":"303",
         "price":"160.55",
         "sales-tax-id":"b97fd7c8-c322-4f1a-95ed-b147ea40880b",
         "sells-by-weight":false,
         "sku":null,
         "created-at":"2019-02-07T10:48:49.000+01:00",
         "updated-at":"2019-03-19T16:50:24.247+01:00"
      },
      "relationships":{
         "company":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/products/00f3b8cd-a0fa-4ba2-a95a-3d3799957c6c/relationships/company",
               "related":"https://api.nextposit.nl/api/v31/products/00f3b8cd-a0fa-4ba2-a95a-3d3799957c6c/company"
            }
         },
         "sales-tax":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/products/00f3b8cd-a0fa-4ba2-a95a-3d3799957c6c/relationships/sales-tax",
               "related":"https://api.nextposit.nl/api/v31/products/00f3b8cd-a0fa-4ba2-a95a-3d3799957c6c/sales-tax"
            }
         }
      }
   }
}
```

### Attributes

| Name                        | Format    |  Description        |
| --------------------------- | --------- | ------------------- |
| description                 | string    |
| name                        | string    | *required*
| plu                         | string    | *required, unique*
| price                       | float     | price before tax in cents
| price-with-tax              | float     | price
| sales-tax-id                | uuid      | id of an existing SalesTax
| sells-by-weight             | boolean   |
| text-allergens              | string    |
| text-allergen_traces        | string    |
| text-ingredients            | string    |
| sku                         | integer   |
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*


### Filters

| Parameter                   | Format    |  Partial Matches    |  Allowed values  |
| --------------------------- | --------- | ------------------- | ---------------- |
| name                        | string    |  Y                  |                  |
| plu                         | string    |  N                  |                  |
| sku                         | integer   |  N                  |                  |
| created-after               | timestamp |  N/A                |                  |
| updated-after               | timestamp |  N/A                |                  |

### Relationships

* [SalesTax](#salestaxes)


### Examples

__Create an product with price including sales_tax__

Assuming SalesTax has a tax percentage 9:

POST an product with an associated tax rate


<div class="center-column"></div>
```
POST /api/v3/products
```

<div class="center-column"></div>
```json
{
  "data": {
    "type": "products",
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

PATCH the product with it's price including taxes

<div class="center-column"></div>
```
PATCH /api/v3/products/d8b55c93-6c08-4a57-a67f-d0a0dc52a288
```
<div class="center-column"></div>
```json
{
  "data": {
    "id": "d8b55c93-6c08-4a57-a67f-d0a0dc52a288",
    "type": "products",
    "attributes": {
      "price-with-tax": 1090
    }
  }
}
```

Results in the following product

<div class="center-column"></div>
```json
{
  "data": {
    "id": "d95e8ced-f845-48db-be9d-2278c42ff30c",
    ...
    "attributes": {
      "price": "1000.0",
      "price-with-tax": 1090,
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