## Articles

Articles add additional information to products required in the rest of the Exposit application.

> Example Address

```json
{
  "data": {
    "id": "4c175fbe-13c5-4eef-a0b9-4f3fe1732d62",
    "type": "articles",
    "links": {
      "self": "https://api.nexposit.nl/api/v3/articles/4c175fbe-13c5-4eef-a0b9-4f3fe1732d62"
    },
    "attributes": {
      "fixed-base-price": "469.0",
      "fixed-base-price-with-tax": 567,
      "name": "Spaghetti Bolognese",
      "sku": "B000A3K6TM",
      "plu": 4351,
      "created-at": "2018-11-02T11:56:51.080+01:00",
      "updated-at": "2018-11-02T11:56:51.080+01:00"
    },
    "relationships": {
      "components": {
        "links": {
          "self": "https://api.nexposit.nl/api/v3/articles/4c175fbe-13c5-4eef-a0b9-4f3fe1732d62/relationships/components",
          "related": "https://api.nexposit.nl/api/v3/articles/4c175fbe-13c5-4eef-a0b9-4f3fe1732d62/components"
        }
      },
      "selections": {
        "links": {
          "self": "https://api.nexposit.nl/api/v3/articles/4c175fbe-13c5-4eef-a0b9-4f3fe1732d62/relationships/selections",
          "related": "https://api.nexposit.nl/api/v3/articles/4c175fbe-13c5-4eef-a0b9-4f3fe1732d62/selections"
        }
      },
      "tags": {
        "links": {
          "self": "https://api.nexposit.nl/api/v3/articles/4c175fbe-13c5-4eef-a0b9-4f3fe1732d62/relationships/tags",
          "related": "https://api.nexposit.nl/api/v3/articles/4c175fbe-13c5-4eef-a0b9-4f3fe1732d62/tags"
        }
      },
      "company": {
        "links": {
          "self": "https://api.nexposit.nl/api/v3/articles/4c175fbe-13c5-4eef-a0b9-4f3fe1732d62/relationships/company",
          "related": "https://api.nexposit.nl/api/v3/articles/4c175fbe-13c5-4eef-a0b9-4f3fe1732d62/company"
        }
      },
      "sales-tax": {
        "links": {
          "self": "https://api.nexposit.nl/api/v3/articles/4c175fbe-13c5-4eef-a0b9-4f3fe1732d62/relationships/sales-tax",
          "related": "https://api.nexposit.nl/api/v3/articles/4c175fbe-13c5-4eef-a0b9-4f3fe1732d62/sales-tax"
        }
      }
    }
  }
}
```

### Attributes

| Name                        | Format    |  Description        |
| --------------------------- | --------- | ------------------- |
| fixed-base-price            | float     |  pre-tax price, overrides calculated price of underlying products
| fixed-base-price-with-tax   | string    |
| name                        | string    | *required, unique*
| sku                         | enum      |
| plu                         | boolean   |
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*

### Relationships

* [Company](#companies)
* [SalesTax](#salestaxes)
* [Components](#components)
* [Selections](#selections)
* [Tags](#tags)
