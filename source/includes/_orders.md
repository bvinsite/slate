## Orders


> Example Order

```json
{
   "data":{
      "id":"d88e571c-9580-4a47-b980-1a8ce7bcf795",
      "type":"orders",
      "links":{
         "self":"https://api.nextposit.nl/api/v31/orders/d88e571c-9580-4a47-b980-1a8ce7bcf795"
      },
      "attributes":{
         "attendant":"Niek",
         "completed-at":"2019-03-21T12:07:14.942+01:00",
         "customer-address":"Geurinklaan 614b",
         "customer-city":"Oud Thierryveld",
         "customer-name":"Agnes Beukema",
         "customer-remark":"",
         "customer-phone":"034112345678",
         "customer-postal-code":"1720 YC",
         "delivery-at":null,
         "number":1,
         "payment-completed":null,
         "pickup-at":"2019-03-22T13:00:00.000+01:00",
         "targeted-at":"2019-03-22T13:00:00.000+01:00",
         "created-at":"2019-03-21T12:01:29.975+01:00",
         "updated-at":"2019-03-21T12:07:14.945+01:00"
      },
      "relationships":{
         "company":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/orders/d88e571c-9580-4a47-b980-1a8ce7bcf795/relationships/company",
               "related":"https://api.nextposit.nl/api/v31/orders/d88e571c-9580-4a47-b980-1a8ce7bcf795/company"
            }
         },
         "customer":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/orders/d88e571c-9580-4a47-b980-1a8ce7bcf795/relationships/customer",
               "related":"https://api.nextposit.nl/api/v31/orders/d88e571c-9580-4a47-b980-1a8ce7bcf795/customer"
            }
         },
         "order-lines":{
            "links":{
               "self":"https://api.nextposit.nl/api/v31/orders/d88e571c-9580-4a47-b980-1a8ce7bcf795/relationships/order-lines",
               "related":"https://api.nextposit.nl/api/v31/orders/d88e571c-9580-4a47-b980-1a8ce7bcf795/order-lines"
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
| created_after               | timestamp |  N/A
| updated_after               | timestamp |  N/A


### Relationships

* [Customer](#customers)
* [OrderLines](#orderlines)
