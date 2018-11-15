## Tags

Tags are used to categorize Products or Articles


> Example Tag

```json
{
  "data": {
    "id": "eb5ff8cf-74a1-402d-9495-d17ef88ecc14",
    "type": "components",
    "links": {
      "self": "https://api.nexposit.nl/api/v3/components/eb5ff8cf-74a1-402d-9495-d17ef88ecc14"
    },
    "attributes": {
      "count": null,
      "fixed-price": null,
      "weight": 150,
      "created-at": "2018-11-02T11:56:51.082+01:00",
      "updated-at": "2018-11-02T11:56:51.082+01:00"
    },
    "relationships": {
      "article": {
        "links": {
          "self": "https://api.nexposit.nl/api/v3/components/eb5ff8cf-74a1-402d-9495-d17ef88ecc14/relationships/article",
          "related": "https://api.nexposit.nl/api/v3/components/eb5ff8cf-74a1-402d-9495-d17ef88ecc14/article"
        }
      },
      "company": {
        "links": {
          "self": "https://api.nexposit.nl/api/v3/components/eb5ff8cf-74a1-402d-9495-d17ef88ecc14/relationships/company",
          "related": "https://api.nexposit.nl/api/v3/components/eb5ff8cf-74a1-402d-9495-d17ef88ecc14/company"
        }
      },
      "product": {
        "links": {
          "self": "https://api.nexposit.nl/api/v3/components/eb5ff8cf-74a1-402d-9495-d17ef88ecc14/relationships/product",
          "related": "https://api.nexposit.nl/api/v3/components/eb5ff8cf-74a1-402d-9495-d17ef88ecc14/product"
        }
      }
    }
  }
}
```

### Attributes

| Name                        | Format    |  Description        |
| --------------------------- | --------- | ------------------- |
| count                       | integer   |  when defined, weight must be null
| fixed-price                 | float     |  pre-tax price, overrides calculated price of underlying products
| weight                      | integer   |  when defined, count must be null
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*



### Relationships

* [Article](#articles)
* [Product](#products)
