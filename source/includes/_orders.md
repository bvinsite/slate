## Orders


> Example Order

```json
{
    "data": {
        "id": "02948a3c-ebd4-4d35-b219-2a7c4a900e79",
        "type": "orders",
        "links": {
            "self": "https://api.nexposit.nl/api/v3/orders/02948a3c-ebd4-4d35-b219-2a7c4a900e79"
        },
        "attributes": {
          "attendant": "",
          "completed-at": "2018-12-03T13:52:05.272+01:00",
          "customer-address": "Aalbertstraat 972",
          "customer-city": "Oud Aalbert aan de Rijn",
          "customer-name": "Bard den Ven",
          "customer-remark": "",
          "customer-phone": "",
          "customer-postal-code": "8042 JL",
          "delivery-at": null,
          "number": null,
          "payment-completed": "2018-12-03T13:51:05.272+01:00",
          "pickup-at": "2018-12-06T14:00:00.000+01:00",
          "targeted-at": "2018-12-06T14:00:00.000+01:00",
          "created-at": "2018-12-03T11:51:05.272+01:00",
          "updated-at": "2018-12-03T11:51:05.272+01:00"
        },
        "relationships": {
            "company": {
                "links": {
                    "self": "https://api.nexposit.nl/api/v3/orders/02948a3c-ebd4-4d35-b219-2a7c4a900e79/relationships/company",
                    "related": "https://api.nexposit.nl/api/v3/orders/02948a3c-ebd4-4d35-b219-2a7c4a900e79/company"
                }
            },
            "customer": {
                "links": {
                    "self": "https://api.nexposit.nl/api/v3/orders/02948a3c-ebd4-4d35-b219-2a7c4a900e79/relationships/customer",
                    "related": "https://api.nexposit.nl/api/v3/orders/02948a3c-ebd4-4d35-b219-2a7c4a900e79/customer"
                }
            },
            "order-lines": {
                "links": {
                    "self": "https://api.nexposit.nl/api/v3/orders/02948a3c-ebd4-4d35-b219-2a7c4a900e79/relationships/order-lines",
                    "related": "https://api.nexposit.nl/api/v3/orders/02948a3c-ebd4-4d35-b219-2a7c4a900e79/order-lines"
                }
            }
        }
    }
}

```

### Attributes

| Name                        | Format    |  Description        |
| --------------------------- | --------- | ------------------- |
| attendant                   | string    |  Identifies which attendant took the order
| completed-at                | timestamp |  Indicates the time at order finalization
| customer-address            | string    |
| customer-city               | string    |
| customer-name               | string    |
| customer-remark             | string    |
| customer-phone              | string    |
| customer-postal-code        | string    |
| delivery-at                 | timestamp | Indicates the time for order delivery. When defined, pickup-at must be null
| number                      | integer   |
| payment-completed           | timestamp | Indicates the time for completing an only payment
| pickup-at                   | timestamp | Indicates the time for order pickup. When defined, delivery-at must be null
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*

### Filters

| Parameter                   | Format    |  Partial Matches    |
| --------------------------- | --------- | ------------------- |
| completed                   | boolean   |  N/A
| completed_after             | timestamp |  N/A
| updated_after               | timestamp |  N/A


### Relationships

* [Customer](#customers)
* [OrderLines](#orderlines)
