## Companies

Provides read only access to the company resource related to the API key. Provided for convenience.

> Example Company

```json
{
   "data":{
      "id":"422dc9d8-b9ff-4afd-95de-a12142abf49a",
      "type":"companies",
      "links":{
         "self":"http://api.lvh.me:3000/api/v31/companies/422dc9d8-b9ff-4afd-95de-a12142abf49a"
      },
      "attributes":{
         "name":"Demo Inc.",
         "manager-subdomain":"demo"
      },
      "relationships":{
...
      }
   },
   "meta":{
      "info":{
...
      }
   }
}

```

### Attributes

| Name                        | Format    |  Description        |
| --------------------------- | --------- | ------------------- |
| name                        | string    |
| manager_subdomain           | string    | Subdomain to access the web backend

### Relationships

* [Addresses](#adresses)
* [Articles](#articles)
* [Orders](#orders)
* [Products](#products)
* [Tags](#tags)



