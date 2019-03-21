# Resources

## Addresses

> Example Address

```json
{
  "data": {
    "id": "06c780c0-36f2-4cd7-8f67-6cb536e448ee",
    "type": "addresses",
    "links": {
        "self": "https://api.nextposit.nl/api/v31/addresses/06c780c0-36f2-4cd7-8f67-6cb536e448ee"
    },
    "attributes": {
        "city": "Pamaingen",
        "postal-code": "5818 SF",
        "street-address": "Martelaan 941",
        "variant": "visiting",
        "primary": false,
        "created-at": "2019-03-14T16:56:48.851+01:00",
        "updated-at": "2019-03-14T16:56:48.851+01:00"
    }
  }
}
```

### Attributes

| Name           | Format    |  Description           |
| -------------- | --------- | ---------------------- |
| city           | string    |
| postal-code    | string    |
| street-address | string    |
| variant        | enum      | one of billing, mailing, shipping, visiting
| primary        | boolean   | one primary address allowed per variant
| created-at     | timestamp | *read-only*
| updated-at     | timestamp | *read-only*


### Filters

| Parameter                   | Format    |  Partial Matches    |
| --------------------------- | --------- | ------------------- |
| primary                     | boolean   |  N/A
| variant                     | string    |  N
| created_after               | timestamp |  N/A
| updated_after               | timestamp |  N/A