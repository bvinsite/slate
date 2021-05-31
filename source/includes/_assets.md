## Assets

Work with the company image collection.


> Example Asset

```json
{
    "data": {
        "id": "0027ac85-a1c6-42ff-9a0a-7066d92ccdca",
        "type": "assets",
        "links": {
            "self": "https://api.nextposit.nl/api/v31/assets/0027ac85-a1c6-42ff-9a0a-7066d92ccdca"
        },
        "attributes": {
            "base64": "/9j/4AAQSkZJR ... NSWjR//Z\n",
            "name": "afbeelding.jpg",
            "created-at": "2020-01-27T14:37:27.388620+01:00",
            "updated-at": "2020-02-15T14:40:06.956048+01:00"
        },
        "relationships": {
            "articles": {
                "links": {
                    "self": "https://api.nextposit.nl/api/v31/assets/0027ac85-a1c6-42ff-9a0a-7066d92ccdca/relationships/articles",
                    "related": "https://api.nextposit.nl/api/v31/assets/0027ac85-a1c6-42ff-9a0a-7066d92ccdca/articles"
                }
            }
        }
    }
}


```

### Attributes

| Name                        | Format    |  Description        |
| --------------------------- | --------- | ------------------- |
| base64                      | string    | Base64 encoded image data
| name                        | string    | Sets the filename for encoded file
| created-at                  | timestamp | *read-only*
| updated-at                  | timestamp | *read-only*

### Relationships

* [Articles](#articles)



