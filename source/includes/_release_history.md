# Release History

## v3.1.6

**Date:** 2019-07-12

Added external reference to order

## v3.1.5

**Date:** 2019-05-31

Added article-name to order-line resource

## v3.1.4

**Date:** 2019-05-2

Feature release

### Features

Added the read-only attribute sells-by-weight? to Article resource


## v3.1.3

**Date:** 2019-05-1

Feature release

### Features

Implemented name filter for tags and added attribute unit_name for articles.

## v3.1.2

**Date:** 2019-04-19

Feature release

### Compatibility

Potential compatibility issues:

None

### Bug fixes

  - Some Documentation fixes

### Features

- Added number to filters for the orders endpoint
- customer-email attribute added to orders endpoint

## v3.1.1

**Date:** 2019-03-21

Bugfix release

### Compatibility

Potential compatibility issues:

- Filters on boolean columns, now return an error when filtering on anything other than [t, f, true, false, 0, 1]
- Filters on enum fields, now return an error when filtering on strings not in the expected list of options


### Bug fixes

  - Fixed crash on created-after filter on some resources
  - Fixed crash on updated-after filter on some resources

### Features

Implemented primary and variant filters for addresses.

## v3.1.0

**Date:** 2019-03-20

Feature release

### Compatibility

Paginated responses are _only_ allowed to user either number/size for paged pagination, or offset/limit for offset pagination. Specifying parameters for both stratgies will result in an error response.

The deprecated attribute name removed from order. Use customer-name, to set a customer name on the order.

### Features

Implemented a Paged Paginator. The paginator can be selected in the request by including

- page[offset] and page[limit] parameters, or
- page[number] and page[size] parameters

## v3.0.6

**Date:** 2018-12-06

Feature/ bugfix release

### Features

- Adds delivery_at / targeted_at filters to

## v3.0.5

**Date:** 2018-11-07

First public release of the v3 API

## v3.0.0


