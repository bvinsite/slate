# Errors

## HTTP response codes

The API will respond with an appropriate HTTP response header when encountering an error.

HTTP Status | Description
----------- | -----------
400         | **Bad request** Returned when an error has occurred. Most likely whenever wrong or incomplete JSON has been transmitted.
403         | **Forbidden** Returned when authentication is invalid or privileges are not enough.
404         | **Not Found** Returned when the requested resource does not exist. For example, the product or order does not exist.
500         | **Internal Error** Returned when an unexpected server side error has occurred.

## Error Response

> Example error response

```json
{
  "errors": [
    {
      "title": "Param not allowed",
      "detail": "sur_name is not allowed.",
      "code": "105",
      "status": "400"
    }
  ]
}
```

Additional error information may be provided in the body of an error response. A human readable
"title" indicates the type of error that has occurred. the "detail" attribute may provide further
information about the cause oth error, for example indicating the attribute causing the error.
The code attribute can be one of the codes listed in the table below.

Error Code | Meaning | Error Code | Meaning
---------- | ------- | ---------- | -------
100 | Validation error | 101 | Invalid resource
102 | Filter not allowed | 103 | Invalid field value
104 | Invalid field | 105 | Param not allowed
106 | Param mising | 107 | Invalid filter value
108 | Count mismatch | 109 | Key order mismatch
100 | Key not included in URL | 112 | Invalid include
113 | Relation Exists | 114 | Invalid sort criteria
115 | Invalid links object | 116 | Type mismatch
117 | Invalid page object | 118 | Invalid page value
119 | Invalid field format | 120 | Invalid filters syntax
121 | Save failed | 403 | Forbidden
404 | Record not found | 406 | Not acceptable
415 | Unsupported media type | 423 | Locked
