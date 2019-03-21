## Tags

Tags are used to categorize Products or Articles


> Example Tag

```json
{
   "data":{
      "id":"03b970bd-bacd-4e23-ab89-d55cca0159d9",
      "type":"tags",
      "links":{
         "self":"https://api.nextposit.nl/api/v31/tags/03b970bd-bacd-4e23-ab89-d55cca0159d9"
      },
      "attributes":{
         "description":null,
         "name":"soepen",
         "primary":null,
         "rank":null,
         "created-at":"2019-03-19T16:50:13.298+01:00",
         "updated-at":"2019-03-19T16:50:13.298+01:00"
      },
      "relationships":{
         "company":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/tags/03b970bd-bacd-4e23-ab89-d55cca0159d9/relationships/company",
               "related":"https://api.nextposit.nl/api/v31/tags/03b970bd-bacd-4e23-ab89-d55cca0159d9/company"
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
| fixed-price                 | float     |  pre-tax price, overrides calculated price of underlying products
| weight                      | integer   |  when defined, count must be null
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*

### Filters

| Parameter                   | Format    |  Partial Matches    |
| --------------------------- | --------- | ------------------- |
| created_after               | timestamp |  N/A
| updated_after               | timestamp |  N/A

### Relationships

* [Article](#articles)
* [Product](#products)
