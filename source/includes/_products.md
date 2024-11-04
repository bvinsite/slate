## Products



> Example Product

```json
{
    "data": {
        "id": "000ab790-2391-4e2f-abec-f3aca9e0fe8f",
        "type": "products",
        "links": {
            "self": "https://api.nextposit.nl/api/v31/products/000ab790-2391-4e2f-abec-f3aca9e0fe8f"
        },
        "attributes": {
            "description": null,
            "name": "Tomatensap",
            "origin": null,
            "plu": "1083",
            "price": "127.52",
            "price-with-tax": 139,
            "sales-tax-id": "a6554faf-3c23-4010-b3fa-f951b491268f",
            "sells-by-weight": false,
            "sku": "ST",
            "text-allergens": null,
            "text-allergen-traces": null,
            "text-ingredients": null,
            "energy": null,
            "fats": null,
            "carbo-hydrates": null,
            "sugars": null,
            "proteins": null,
            "salt": null,
            "discarded-at": null,
            "created-at": "2021-11-05T15:52:26.281659+01:00",
            "updated-at": "2023-10-03T11:56:20.056474+02:00"
        },
        "relationships": {
            "company": {
                "links": {
                    "self": "https://api.nextposit.nl/api/v31/products/000ab790-2391-4e2f-abec-f3aca9e0fe8f/relationships/company",
                    "related": "https://api.nextposit.nl/api/v31/products/000ab790-2391-4e2f-abec-f3aca9e0fe8f/company"
                }
            },
            "sales-tax": {
                "links": {
                    "self": "https://api.nextposit.nl/api/v31/products/000ab790-2391-4e2f-abec-f3aca9e0fe8f/relationships/sales-tax",
                    "related": "https://api.nextposit.nl/api/v31/products/000ab790-2391-4e2f-abec-f3aca9e0fe8f/sales-tax"
                }
            }
        }
    },
    "meta": {
        "info": {
            "version": "v3.1.18",
            "publisher": "Bon Vivant In-site",
            "documentation": "https://apidocs.nextposit.nl/",
            "email": "apiteam@exposit.nl"
        }
    }
}


```

### Attributes

| Name                        | Format    |  Description        |
| --------------------------- | --------- | ------------------- |
| description                 | string    |
| name                        | string    | *required*
| origin                      | string    | Country or region of origin
| plu                         | string    | *required, unique*
| price                       | float     | Price before tax in cents
| price-with-tax              | float     | Price
| sales-tax-id                | uuid      | An existing SalesTax uuid
| sells-by-weight             | boolean   |
| sku                         | integer   |
| text-allergens              | string    |
| text-allergen-traces        | string    |
| text-ingredients            | string    |
| energy                      | integer   | In kJ per 100g/ 100ml
| fats                        | integer   | In gram per 100g/ 100ml
| carbo-hydrates              | integer   | In gram per 100g/ 100ml
| sugars                      | integer   | In gram per 100g/ 100ml
| proteins                    | integer   | In gram per 100g/ 100ml
| salt                        | integer   | In gram per 100g/ 100ml
| discarded-at                | timestamp | Made obsolete at this time
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*


### Filters

| Parameter                   | Format    |  Partial Matches    |  Allowed values  |
| --------------------------- | --------- | ------------------- | ---------------- |
| name                        | string    |  Y                  |                  |
| plu                         | string    |  N                  |                  |
| sku                         | integer   |  N                  |                  |
| created-after               | timestamp |  N/A                |                  |
| updated-after               | timestamp |  N/A                |                  |

### Relationships

* [SalesTax](#salestaxes)


### Examples

__Create an product with price including sales_tax__

Assuming SalesTax has a tax percentage 9:

POST an product with an associated tax rate


<div class="center-column"></div>
```
POST /api/v3/products
```

<div class="center-column"></div>
```json
{
  "data": {
    "type": "products",
    "attributes": {
      "plu": "1000001",
      "name": "Test Article I",
    },
    "relationships": {
      "sales-tax": {
        "data": {
          "type": "sales-taxes",
          "id": "acc97298-ab78-498f-82f6-73d8e9c803bd"
        }
      }
    }
  }
}
```

PATCH the product with it's price including taxes

<div class="center-column"></div>
```
PATCH /api/v3/products/d8b55c93-6c08-4a57-a67f-d0a0dc52a288
```
<div class="center-column"></div>
```json
{
  "data": {
    "id": "d8b55c93-6c08-4a57-a67f-d0a0dc52a288",
    "type": "products",
    "attributes": {
      "price-with-tax": 1090
    }
  }
}
```

Results in the following product

<div class="center-column"></div>
```json
{
  "data": {
    "id": "d95e8ced-f845-48db-be9d-2278c42ff30c",
    ...
    "attributes": {
      "price": "1000.0",
      "price-with-tax": 1090,
      ...
    },
    "relationships": {
      ...
      }
    }
  },
  "meta": {...}
}
```