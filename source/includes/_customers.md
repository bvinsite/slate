## Customers


> Example Customer

```json
{
    "data": {
        "id": "060b16de-0a19-4aaf-9be5-62197e55a2e8",
        "type": "customers",
        "links": {
            "self": "http://api.lvh.me:3000/api/v3/customers/060b16de-0a19-4aaf-9be5-62197e55a2e8"
        },
        "attributes": {
            "email": "montevonrueden@langosh.name",
            "name": "Kemberly Thompson",
            "number": 8,
            "created-at": "2018-11-02T11:56:51.200+01:00",
            "updated-at": "2018-11-02T11:56:51.200+01:00"
        },
        "relationships": {
            "company": {
                "links": {
                    "self": "http://api.lvh.me:3000/api/v3/customers/060b16de-0a19-4aaf-9be5-62197e55a2e8/relationships/company",
                    "related": "http://api.lvh.me:3000/api/v3/customers/060b16de-0a19-4aaf-9be5-62197e55a2e8/company"
                }
            },
            "orders": {
                "links": {
                    "self": "http://api.lvh.me:3000/api/v3/customers/060b16de-0a19-4aaf-9be5-62197e55a2e8/relationships/orders",
                    "related": "http://api.lvh.me:3000/api/v3/customers/060b16de-0a19-4aaf-9be5-62197e55a2e8/orders"
                }
            },
            "addresses": {
                "links": {
                    "self": "http://api.lvh.me:3000/api/v3/customers/060b16de-0a19-4aaf-9be5-62197e55a2e8/relationships/addresses",
                    "related": "http://api.lvh.me:3000/api/v3/customers/060b16de-0a19-4aaf-9be5-62197e55a2e8/addresses"
                }
            }
        }
    },
    "meta": {
        "info": {
            "version": "v3.0.5",
            "publisher": "Bon Vivant In-site",
            "documentation": "https://api.exposit.nl/api/docs/v20",
            "email": "apiteam@exposit.nl"
        }
    }
}

```

### Attributes

| Name                        | Format    |  Description        |
| --------------------------- | --------- | ------------------- |
| email                       | string    |
| name                        | string    |
| number                      | integer   | Unique customer number
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*

### Filters

| Parameter                   | Format    |  Partial Matches    |
| --------------------------- | --------- | ------------------- |
| email                       | string    |  N
| name                        | string    |  Y
| number                      | integer   |  N

### Relationships

* [Company](#companies)
* [Addresses](#adresses)
* [Orders](#orders)



