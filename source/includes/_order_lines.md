## OrderLines



> Example OrderLine

```json
{
    "data": {
        "id": "06ab8a5f-f342-47f2-b5e5-ea222828ab9d",
        "type": "order-lines",
        "links": {
            "self": "https://api.nexposit.nl/api/v3/order-lines/06ab8a5f-f342-47f2-b5e5-ea222828ab9d"
        },
        "attributes": {
            "article-plu": 4351,
            "count": 6,
            "customer-remark": null,
            "total-price": "2814.0",
            "unit-price": "469.0",
            "sales-tax-id": "b3081629-ec17-4dac-9764-97e4f4f03256",
            "weight": null,
            "created-at": "2018-11-02T11:56:53.645+01:00",
            "updated-at": "2018-11-02T11:56:53.673+01:00"
        },
        "relationships": {
            "article": {
                "links": {
                    "self": "https://api.nexposit.nl/api/v3/order-lines/06ab8a5f-f342-47f2-b5e5-ea222828ab9d/relationships/article",
                    "related": "https://api.nexposit.nl/api/v3/order-lines/06ab8a5f-f342-47f2-b5e5-ea222828ab9d/article"
                }
            },
            "company": {
                "links": {
                    "self": "https://api.nexposit.nl/api/v3/order-lines/06ab8a5f-f342-47f2-b5e5-ea222828ab9d/relationships/company",
                    "related": "https://api.nexposit.nl/api/v3/order-lines/06ab8a5f-f342-47f2-b5e5-ea222828ab9d/company"
                }
            },
            "order": {
                "links": {
                    "self": "https://api.nexposit.nl/api/v3/order-lines/06ab8a5f-f342-47f2-b5e5-ea222828ab9d/relationships/order",
                    "related": "https://api.nexposit.nl/api/v3/order-lines/06ab8a5f-f342-47f2-b5e5-ea222828ab9d/order"
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


### Relationships

* [Article](#articles)
* [Order](#order)
