## Tags

Tags are used to categorize Articles


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
         "external-reference":null,
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
| description                 | string    |
| external-reference          | string    | Reference to id in external systems
| name                        | string    |  *unique*
| primary                     | boolean   |  primary tags are displayed more prominently
| rank                        | integer   |  used to order tags
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*

### Filters

| Parameter                   | Format    |  Partial Matches    |  Allowed values  |
| --------------------------- | --------- | ------------------- | ---------------- |
| name                        | string    |  N                  |                  |
| created-after               | timestamp |  N/A                |                  |
| updated-after               | timestamp |  N/A                |                  |

### Relationships

* [Company](#companies)
