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
