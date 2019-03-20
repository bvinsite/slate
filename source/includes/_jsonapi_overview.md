# JSON:API Overview

The Exposit API implements the JSON API specification. This means there are some notable semantics to how you consume it, but understanding it will take a lot of the work of using it out of your hands.

These docs will include a short overview of the capabilities, but you can consult the [JSON API Specification](http://jsonapi.org/format/) for more information.

You can be more specific about the data you want to retrieve by using URL parameters outlined below.

## Client Implementations

Since JSON API is standardised, API-agnostic tools can be made to abstract away the semantics of consuming and working with the data. These resources can be a great help in working with the requesting and working with the data.

Implementations in a number of languages can be found on the [JSON API website](https://jsonapi.org/implementations/#client-libraries).

## Request Headers


As per the JSON:API specification on on [content negotiation]
(https://jsonapi.org/format/#content-negotiation), make sure to send the required Content-Type
header when sending data to the API
<pre>
Accept: application/vnd.api+json
Content-Type: application/vnd.api+json
</pre>

## Filtering and Search

> Filtered request example

```
  /orders?filter[finalised-after]=2001-12-31
  /orders?filter[finalised-after]=2001-12-31
```

Filtering lets you query data that contains certain matching attributes or relationships.

These take the form of filter[name]=value. As an example, you can ask the API to retrn all orders
create after a timestamp


## Pagination

You can choose how much of a resource to receive by specifying pagination parameters. Pagination is
supported via offset or page. Resources are paginated in groups of 50 by default.


### Offset pagination

> Offset request example

```
/orders?page[offset]=50
/orders?page[limit]=25&page[offset]=50
```

The offset paginator returns results based on an offset from the beginning of the resultset. Valid page parameters are *page[offset]* and *page[limit]*.


### Paged pagination

> Paged request example

```
/orders?page[number]=2
/orders?page[number]=3&page[size]=25
```

The offset paginator returns results based on page number and page size.  Valid page parameters are *page[number]* and *page[size]*.


### Paginated response

> Example Response

<pre>
    "links":{
        "first": "...?page%5Blimit%5D=50&page%5Boffset%5D=0",
        "prev": "...?page%5Blimit%5D=50&page%5Boffset%5D=4",
        "next": "...?page%5Blimit%5D=50&page%5Boffset%5D=6",
        "last": "...?page%5Blimit%5D=50&page%5Boffset%5D=45"
    }
</pre>

The response will include URLs for the first, previous, next and last page of resources in the links object
based on your request.


## Sorting


> Sorted request example

```
/customers?sort=-number,name
```

Sorting by attributes is also supported. By default, sorts are applied in ascending order. You can
request a descending order by prepending - to the parameter. You can use a comma-delimited list to
sort by multiple attributes.


## Includes

> Include request example

```
/order?include=order-lines.article,customer
```

Related resources can be requested in the reponse with include=[relationship]. You can also
specify successive  relationships using a .. A comma-delimited list can be used to request
multiple relationships.


## Sparse Fieldsets

> Sparse ields request example

```
/product?fields=name,plu
```



You can request a resource to only return a specific set of fields in its response.