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
            "attendant": null,
            "completed-at": "2018-11-02T11:56:53.714+01:00",
            "customer-address": null,
            "customer-city": null,
            "customer-name": null,
            "customer-remark": null,
            "customer-phone": null,
            "customer-postal-code": null,
            "name": "Sina Wiegand",
            "number": 25,
            "payment-completed": null,
            "pickup-at": "2018-10-28T05:39:33.635+01:00",
            "created-at": "2018-11-02T11:56:53.639+01:00",
            "updated-at": "2018-11-02T11:56:53.715+01:00"
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
| number                      | integer   |
| payment-completed           | boolean   |
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*



### Relationships

* [Customer](#customers)
* [OrderLines](#orderlines)
