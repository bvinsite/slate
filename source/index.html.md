---
title: Exposit API (v3.0.5)

language_tabs: # must be one of https://git.io/vQNgJ

toc_footers:
  - Een Bon Vivant In-site project
  - Email our <a href="mailto:apiteam@exposit.nl">API team</a>
  - <a href='https://github.com/lord/slate'>Documentation Powered by Slate</a>

includes:
  - introduction
  - addresses
  - articles
  - components
  - customers
  - orders
  - order_lines
  - products
  - sales_taxes
  - errors

search: true
---

# Introduction

The Exposit API, by Bon Vivant In-site (the API) follows the [JSON API v1.0](https://jsonapi.org/format/).

A list of libraries implementing JSON:API is available at: [https://jsonapi.org/implementations/](https://jsonapi.org/implementations/)

For example, when version 3.2.12 is the latest published API version, the API versions are available at the following URIs:


| Base Path     | API Version  |
| ------------- |:--------------|
| /api/v3       | v.3.2.12      |
| /api/v31      | v.3.1.x       |
| /api/v32      | v.3.2.12      |


# Versioning

Versioning folllows the major.minor.micro format.

**Micro versions**

Micro version changes present no or very limited risks to compatibility.

For example: Micro versions may introduce new attributes, endpoints, relationships. Micro versions may relax or
remove restrictions on attribute data types.

**Minor versions**

Minor version changes may present some impact on compatibility.

For example: Minor versions may remove or rename attributes, or relationships. Minor versions may change
attribute data types, tighten restrictions on attribute data types.

**Major versions**

Major version changes signify updates to the API in a potentially incompatible way.




# Authentication

> To authorize, use this code:

```ruby
require 'faraday'

json = Faraday.new('https://api.nextposit.nl/api/v3/customers', headers: { x_api_key: "40d73b963f" }).get
```

```python
import requests

json = requests.get(url, headers={'x-api-key': '40d73b963f'})
```

```shell
# With shell, you can just pass the correct header with each request
curl "https://api.nextposit.nl/api/v3/customers" -H "A-api-key: 40d73b963f"
```

> Make sure to replace `meowmeowmeow` with your API key.

The exposit API uses an API key to access teh API. You can request a new API key by contacting our [API team](apiteam@exposit.nl)

All API request to the server should include the api key in the request header;

`x-api-key: 21f2baabd36866a4664e0056241e22c8`

<aside class="notice">
You must replace <code>21f2baabd36866a4664e0056241e22c8</code> with your API key.
</aside>

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


