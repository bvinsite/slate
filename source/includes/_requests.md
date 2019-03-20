

# Requests

As per the JSON:API specification on on [content negotiation]
(https://jsonapi.org/format/#content-negotiation), make sure to send the required Content-Type
header when sending data to the API

<aside class="notice">
  Clients MUST send all JSON:API data in request documents with the header Content-Type: application/vnd.api+json without any media type parameters.
</aside>

Every resource responds to one or more of the endpoints described in this section




## List resources

> Example response

```json
[
  {
    "id": "0ad6ceaa-839a-446c-ad14-7afd31d8d6cb",
    "type": "products", // The reource type being returned
    "links": {
      "self": "" // The link that generated the current response document.
    },
    "attributes": {
      "plu": "1009",
      "price": 809.02,
      // The current resource's attributes
    },
    "relationships": {
      // ... this article's relationships
    }
  },
  ...
]
```

This endpoint returns a list of resources

### Request

GET */api/v3/resource*


### Response

**200** OK

#### Response body

A JSON array of resources




## Create a resource

This endpoint creates a new resource

### Request

POST */api/v3/resource*

##### Request body

The resource to be created

### Response

**201** Created

#### Response body

The created resource




## Retrieve a resource

This endpoint returns a single resource

### Request

GET */api/v3/resource/$id*

#### URL parameters

| Name | Description |
| ---- | ----------- |
| id   | The resource's id |

##### Request body

The resource to be created

### Response

**200** OK

#### Response body

The requested resource




## Update a resource

This endpoint updates an existing resource

### Request

PATCH */api/v3/resource/$id*

##### Request body

The updated resource, data not present in the request body be left unchanged.

### Response

**200** OK

#### Response body

The updated resource




## Remove a resource

This endpoint removes an existing resource

### Request

DELETE */api/v3/resource/$id*

### Response

**204** No Content

#### Response body

*None*


