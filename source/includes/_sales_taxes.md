## SalesTax

SalesTax is a a read-only resource

> Example SalesTax

```json
{
    "data": {
        "id": "b3081629-ec17-4dac-9764-97e4f4f03256",
        "type": "sales-taxes",
        "links": {
            "self": "https://api.nexposit.nl/api/v3/sales-taxes/b3081629-ec17-4dac-9764-97e4f4f03256"
        },
        "attributes": {
            "name": "Laag",
            "percentage": 6
        },
        "relationships": {
            "articles": {
                "links": {
                    "self": "https://api.nexposit.nl/api/v3/sales-taxes/b3081629-ec17-4dac-9764-97e4f4f03256/relationships/articles",
                    "related": "https://api.nexposit.nl/api/v3/sales-taxes/b3081629-ec17-4dac-9764-97e4f4f03256/articles"
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



### Relationships

**None**