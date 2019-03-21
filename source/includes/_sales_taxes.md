## SalesTaxes

SalesTax is a a read-only resource

> Example SalesTax

```json
{
   "data":{
      "id":"5b38ecd1-0f58-45e9-a8ff-74dfb0075de0",
      "type":"sales-taxes",
      "links":{
         "self":"https://api.nextposit.nl/api/v31/sales-taxes/5b38ecd1-0f58-45e9-a8ff-74dfb0075de0"
      },
      "attributes":{
         "name":"Hoog",
         "percentage":21
      },
      "relationships":{
         "articles":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/sales-taxes/5b38ecd1-0f58-45e9-a8ff-74dfb0075de0/relationships/articles",
               "related":"https://api.nextposit.nl/api/v31/sales-taxes/5b38ecd1-0f58-45e9-a8ff-74dfb0075de0/articles"
            }
         }
      }
   }
}

```

### Attributes

| Name                        | Format    |  Description        |
| --------------------------- | --------- | ------------------- |
| name                        | string    | *read-only*
| percentage                  | integer   | *read-only*

### Filters

| Parameter                   | Format    |  Partial Matches    |
| --------------------------- | --------- | ------------------- |
| created_after               | timestamp |  N/A
| updated_after               | timestamp |  N/A

### Relationships

**None**