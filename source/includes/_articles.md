## Articles

Articles add additional information to products required in the rest of the Exposit application.

> Example Article

```json
{
    "data": {
        "id": "03daa5d5-e564-4404-98d9-d8e586570233",
        "type": "articles",
        "links": {
            "self": "https://api.nextposit.nl/api/v31/articles/03daa5d5-e564-4404-98d9-d8e586570233"
        },
        "attributes": {
            "base-price": 0,
            "base-price-with-tax": 0,
            "components-price": 0,
            "components-price-with-tax": 0,
            "conservation-advice": "",
            "description": null,
            "fixed-base-price": null,
            "fixed-base-price-with-tax": null,
            "in-shop": false,
            "max": null,
            "min": null,
            "name": "Courgette",
            "normal-price": 0,
            "normal-price-with-tax": 0,
            "offer-price-ends-at": null,
            "offer-price-starts-at": null,
            "offer-price-with-tax": null,
            "orderable-ends-at": null,
            "orderable-starts-at": "2024-06-26",
            "sales-tax-id": "a6554faf-3c23-4010-b3fa-f951b491268f",
            "sells-by-weight": null,
            "preparation-advice": null,
            "plu": "541",
            "sku": null,
            "step": null,
            "unit-name": null,
            "discarded-at": null,
            "created-at": "2024-05-01T09:03:28.125374+02:00",
            "updated-at": "2024-05-01T09:03:28.125374+02:00"
        },
        "relationships": {
            "components": {
                "links": {
                    "self": "https://api.nextposit.nl/api/v31/articles/03daa5d5-e564-4404-98d9-d8e586570233/relationships/components",
                    "related": "https://api.nextposit.nl/api/v31/articles/03daa5d5-e564-4404-98d9-d8e586570233/components"
                }
            },
            "selections": {
                "links": {
                    "self": "https://api.nextposit.nl/api/v31/articles/03daa5d5-e564-4404-98d9-d8e586570233/relationships/selections",
                    "related": "https://api.nextposit.nl/api/v31/articles/03daa5d5-e564-4404-98d9-d8e586570233/selections"
                }
            },
            "tags": {
                "links": {
                    "self": "https://api.nextposit.nl/api/v31/articles/03daa5d5-e564-4404-98d9-d8e586570233/relationships/tags",
                    "related": "https://api.nextposit.nl/api/v31/articles/03daa5d5-e564-4404-98d9-d8e586570233/tags"
                }
            },
            "asset": {
                "links": {
                    "self": "https://api.nextposit.nl/api/v31/articles/03daa5d5-e564-4404-98d9-d8e586570233/relationships/asset",
                    "related": "https://api.nextposit.nl/api/v31/articles/03daa5d5-e564-4404-98d9-d8e586570233/asset"
                }
            },
            "company": {
                "links": {
                    "self": "https://api.nextposit.nl/api/v31/articles/03daa5d5-e564-4404-98d9-d8e586570233/relationships/company",
                    "related": "https://api.nextposit.nl/api/v31/articles/03daa5d5-e564-4404-98d9-d8e586570233/company"
                }
            },
            "sales-tax": {
                "links": {
                    "self": "https://api.nextposit.nl/api/v31/articles/03daa5d5-e564-4404-98d9-d8e586570233/relationships/sales-tax",
                    "related": "https://api.nextposit.nl/api/v31/articles/03daa5d5-e564-4404-98d9-d8e586570233/sales-tax"
                }
            }
        }
    },
    "meta": {
        "info": {
            "version": "v3.1.17",
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
| base-price                  | decimal   | *read-only* current base price (without additional selections)
| base-price-with-tax         | integer   | *read-only*
| components-price            | decimal   | *read-only* price of underlying component(s)
| components-price-with-tax   | integer   | *read-only*
| conservation-advice         | string    | Advice on storing and conserving this article
| description                 | string    | Description of the item
| fixed-base-price            | decimal   | Pre-tax price in cents, overrides calculated price of underlying products
| fixed-base-price-with-tax   | integer   | Tax price in cents
| in-shop                     | boolean   | article available to show in webshop(s)
| max                         | integer   | maximum weight/number per orderline in webshop(s)
| min                         | integer   | minimum weight/number per orderline in webshop(s)
| name                        | string    | *required*
| normal-price                | decimal   | *read-only* price before taking into account offers
| normal-price-with-tax       | integer   | *read-only*
| offer-price-ends-at         | timestamp | Offer price valid from
| offer-price-starts-at       | timestamp | Offer price valid until
| offer-price-with-tax        | integer   | Offer price in cents
| orderable-ends-at           | date      | End of availability in the webshop
| orderable-starts-at         | date      | Start of availability in the webshop
| preparation-advice          | string    | May include html mark-up
| plu                         | string    | *required, unique*
| sales-tax-id                | boolean   | An existing SalesTax uuid
| sells-by-weight             | boolean   |
| sku                         | string    |
| step                        | integer   | size of weight/number steps in webshop(s)
| unit-name                   | string    |
| discarded-at                | timestamp | Resource made obsolete at this time
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*

### Filters

| Parameter                   | Format    |  Partial Matches    |  Allowed values  |
| --------------------------- | --------- | ------------------- | ---------------- |
| plu                         | string    |  N                  |                  |
| sku                         | string    |  N                  |                  |
| name                        | string    |  Y                  |                  |
| created-after               | timestamp |  N/A                |                  |
| updated-after               | timestamp |  N/A                |                  |

### Relationships

* [Company](#companies)
* [SalesTax](#salestaxes)
* [Components](#components)
* [Selections](#selections)
* [Tags](#tags)

### Examples

__Create an article with price including sales_tax__

Assuming SalesTax has a tax percentage 9:

POST an article with an associated tax rate


<div class="center-column"></div>
```
POST /api/v3/articles
```

<div class="center-column"></div>
```json
{
  "data": {
    "type": "articles",
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

PATCH the article with it's price including taxes

<div class="center-column"></div>
```
PATCH /api/v3/articles/d8b55c93-6c08-4a57-a67f-d0a0dc52a288
```
<div class="center-column"></div>
```json
{
  "data": {
    "id": "d8b55c93-6c08-4a57-a67f-d0a0dc52a288",
    "type": "articles",
    "attributes": {
      "fixed-base-price-with-tax": 1090
    }
  }
}
```

Results in the following article

<div class="center-column"></div>
```json
{
  "data": {
    "id": "d95e8ced-f845-48db-be9d-2278c42ff30c",
    ...
    "attributes": {
      "fixed-base-price": "1000.0",
      "fixed-base-price-with-tax": 1090,
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