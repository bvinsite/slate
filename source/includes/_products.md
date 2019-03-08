## Products



> Example Product

```json
{
    "data": {
        "id": "0957b78a-1a52-49d2-8a28-7f5d75241114",
        "type": "products",
        "links": {
            "self": "https://api.nexposit.nl/api/v3/products/0957b78a-1a52-49d2-8a28-7f5d75241114"
        },
        "attributes": {
            "description": null,
            "name": "Spaghetti Bolognese",
            "plu": "17169ab",
            "price": 967,
            "sells-by-weight": true,
            "sku": null,
            "created-at": "2018-11-02T11:56:50.639+01:00",
            "updated-at": "2018-11-02T11:56:50.639+01:00"
        },
        "relationships": {
            "company": {
                "links": {
                    "self": "https://api.nexposit.nl/api/v3/products/0957b78a-1a52-49d2-8a28-7f5d75241114/relationships/company",
                    "related": "https://api.nexposit.nl/api/v3/products/0957b78a-1a52-49d2-8a28-7f5d75241114/company"
                }
            },
            "sales-tax": {
                "links": {
                    "self": "https://api.nexposit.nl/api/v3/products/0957b78a-1a52-49d2-8a28-7f5d75241114/relationships/sales-tax",
                    "related": "https://api.nexposit.nl/api/v3/products/0957b78a-1a52-49d2-8a28-7f5d75241114/sales-tax"
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
| sells-by-weight             | boolean   |
| sku                         | integer   |
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*

### Relationships

* [SalesTax](#salestax)
