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
| price                       | float     | price before tax
| sales-tax-id                | uuid      | id of an existing SalesTax
| sells-by-weight             | boolean   |
| sku                         | integer   |
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*


### Filters

| Parameter                   | Format    |  Partial Matches    |  Allowed values  |
| --------------------------- | --------- | ------------------- | ---------------- |
| name                        | string    |  Y                  |                  |
| plu                         | string    |  N                  |                  |
| sku                         | integer   |  N                  |                  |
| created_after               | timestamp |  N/A                |                  |
| updated_after               | timestamp |  N/A                |                  |

### Relationships

* [SalesTax](#salestaxes)
