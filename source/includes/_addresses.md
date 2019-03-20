# Resources

## Addresses

> Example Address

```json
{
  "data": {
  "id": "f5f49914-6506-49e8-8f7a-bb208c470439",
  "type": "addresses",
  "links": {
    "self": "https://api.nexposit.nl/api/v3/addresses/f5f49914-6506-49e8-8f7a-bb208c470439"
  },
    "attributes": {
      "city": "Loganside",
      "name": "9330 Kuphal Hollow",
      "postal-code": "00472",
      "street-address": "9330 Kuphal Hollow",
      "variant": "shipping",
      "primary": true,
      "created-at": "2018-09-02T11:56:52.100+01:00",
      "updated-at": "2018-09-02T11:56:52.100+01:00"
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
| variant        | enum      | one of [:mailing, :shipping, :visiting]
| primary        | boolean   | one primary address allowed per variant
| created-at     | timestamp | *read-only*
| updated-at     | timestamp | *read-only*


### Filters

| Parameter                   | Format    |  Partial Matches    |
| --------------------------- | --------- | ------------------- |
| primary                     | boolean   |  N/A
| variant                     | string    |  N
