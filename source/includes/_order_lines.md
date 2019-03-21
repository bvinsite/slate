## OrderLines



> Example OrderLine

```json
{
   "data":{
      "id":"d6ff62fb-8ddc-4e38-903e-85fd5b94e5e7",
      "type":"order-lines",
      "links":{
         "self":"https://api.nextposit.nl/api/v31/order-lines/d6ff62fb-8ddc-4e38-903e-85fd5b94e5e7"
      },
      "attributes":{
         "article-plu":"104",
         "count":1,
         "customer-remark":"",
         "total-price":"362.39",
         "unit-price":"362.39",
         "weight":null,
         "created-at":"2019-03-21T12:01:38.324+01:00",
         "updated-at":"2019-03-21T12:01:38.324+01:00"
      },
      "relationships":{
         "article":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/order-lines/d6ff62fb-8ddc-4e38-903e-85fd5b94e5e7/relationships/article",
               "related":"https://api.nextposit.nl/api/v31/order-lines/d6ff62fb-8ddc-4e38-903e-85fd5b94e5e7/article"
            }
         },
         "company":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/order-lines/d6ff62fb-8ddc-4e38-903e-85fd5b94e5e7/relationships/company",
               "related":"https://api.nextposit.nl/api/v31/order-lines/d6ff62fb-8ddc-4e38-903e-85fd5b94e5e7/company"
            }
         },
         "order":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/order-lines/d6ff62fb-8ddc-4e38-903e-85fd5b94e5e7/relationships/order",
               "related":"https://api.nextposit.nl/api/v31/order-lines/d6ff62fb-8ddc-4e38-903e-85fd5b94e5e7/order"
            }
         }
      }
   }
}

```

### Attributes

| Name                        | Format    |  Description        |
| --------------------------- | --------- | ------------------- |
| article-plu                 | integer   |
| count                       | integer   |
| customer-remark             | string    |
| total-price                 | decimal   | pre-tax price in cents, total-price is unit-price times count
| unit-price                  | decimal   | pre-tax price in cents, calculated price based on ordered article
| sales-tax-id                | uuid      | id of an existing SalesTax
| weight                      | float     |
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*

### Filters

| Parameter                   | Format    |  Partial Matches    |  Allowed values  |
| --------------------------- | --------- | ------------------- | ---------------- |
| created_after               | timestamp |  N/A                |                  |
| updated_after               | timestamp |  N/A                |                  |

### Relationships

* [Article](#articles)
* [Order](#orders)
