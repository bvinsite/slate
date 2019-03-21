## Components

Components determine the fixed Products making up an Article.

> Example Component

```json
{
   "data":{
      "id":"911e453f-50df-4a55-b263-2111c1b4b0f4",
      "type":"components",
      "links":{
         "self":"https://api.nextposit.nl/api/v31/components/911e453f-50df-4a55-b263-2111c1b4b0f4"
      },
      "attributes":{
         "count":1,
         "fixed-price":"295.0",
         "weight":null,
         "created-at":"2019-03-19T16:50:29.932+01:00",
         "updated-at":"2019-03-19T16:50:29.932+01:00"
      },
      "relationships":{
         "article":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/components/911e453f-50df-4a55-b263-2111c1b4b0f4/relationships/article",
               "related":"https://api.nextposit.nl/api/v31/components/911e453f-50df-4a55-b263-2111c1b4b0f4/article"
            }
         },
         "company":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/components/911e453f-50df-4a55-b263-2111c1b4b0f4/relationships/company",
               "related":"https://api.nextposit.nl/api/v31/components/911e453f-50df-4a55-b263-2111c1b4b0f4/company"
            }
         },
         "product":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/components/911e453f-50df-4a55-b263-2111c1b4b0f4/relationships/product",
               "related":"https://api.nextposit.nl/api/v31/components/911e453f-50df-4a55-b263-2111c1b4b0f4/product"
            }
         }
      }
   }
}
```

### Attributes

| Name                        | Format    |  Description        |
| --------------------------- | --------- | ------------------- |
| count                       | integer   |  when defined, weight must be null
| fixed-price                 | decimal   |  pre-tax price in cents, overrides calculated price of underlying products
| weight                      | integer   |  when defined, count must be null
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*

### Filters

| Parameter                   | Format    |  Partial Matches    |  Allowed values  |
| --------------------------- | --------- | ------------------- | ---------------- |
| created_after               | timestamp |  N/A                |                  |
| updated_after               | timestamp |  N/A                |                  |

### Relationships

* [Article](#articles)
* [Product](#products)
