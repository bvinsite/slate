## Customers


> Example Customer

```json
{
   "data":{
      "id":"05a3cf33-673a-4482-9827-bc518c0f1b80",
      "type":"customers",
      "links":{
         "self":"https://api.nextposit.nl/api/v31/customers/05a3cf33-673a-4482-9827-bc518c0f1b80"
      },
      "attributes":{
         "email":"drew@krajcik.org",
         "name":"Erica van den Kies",
         "number":453,
         "created-at":"2019-03-14T16:56:48.718+01:00",
         "updated-at":"2019-03-14T16:56:48.718+01:00"
      },
      "relationships":{
         "company":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/customers/05a3cf33-673a-4482-9827-bc518c0f1b80/relationships/company",
               "related":"https://api.nextposit.nl/api/v31/customers/05a3cf33-673a-4482-9827-bc518c0f1b80/company"
            }
         },
         "orders":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/customers/05a3cf33-673a-4482-9827-bc518c0f1b80/relationships/orders",
               "related":"https://api.nextposit.nl/api/v31/customers/05a3cf33-673a-4482-9827-bc518c0f1b80/orders"
            }
         },
         "addresses":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/customers/05a3cf33-673a-4482-9827-bc518c0f1b80/relationships/addresses",
               "related":"https://api.nextposit.nl/api/v31/customers/05a3cf33-673a-4482-9827-bc518c0f1b80/addresses"
            }
         }
      }
   }
}

```

### Attributes

| Name                        | Format    |  Description        |
| --------------------------- | --------- | ------------------- |
| email                       | string    | *unique*
| name                        | string    | *unique*
| number                      | integer   | Unique customer number
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*

### Filters

| Parameter                   | Format    |  Partial Matches    |  Allowed values  |
| --------------------------- | --------- | ------------------- | ---------------- |
| email                       | string    |  N                  |                  |
| name                        | string    |  Y                  |                  |
| number                      | integer   |  N                  |                  |

### Relationships

* [Company](#companies)
* [Addresses](#addresses)
* [Orders](#orders)



