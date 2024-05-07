# Release History

## v3.1.17

**Date:** 2024-05-06

Feature release
- Added preparation-advice to article resource

## v3.1.16

**Date:** 2024-04-17

Feature release

- Added text-allergens to products
- Added text-allergen-traces to products
- Added text-ingredients to products

## v3.1.15

**Date:** 2021-02-15

Feature release

- Added assets endpoint
- Added article - asset reference

## v3.1.14

**Date:** 2021-02-15

Feature release

- Added normal-price to articles
- Added normal-price-with-tax to articles

## v3.1.13

**Date:** 2020-11-06

Feature release

- Added components-price to articles
- Added components-price-with-tax to articles

## v3.1.12

**Date:** 2019-11-29

Bugfix release

### Bug fixes

  - Increases response timestamp precision to microseconds

## v3.1.11

**Date:** 2019-11-26

Bugfix release

### Bug fixes

  - Fixes incorrect filtering for created_after/updated_after with some timezones.

## v3.1.10

**Date:** 2019-10-28

Feature release

Made sells-by-weight a read/write attribute on the article resource
Added a price-with-tax attribute to the product resource

## v3.1.9

**Date:** 2019-09-30

Feature release

Added external reference to Tag

## v3.1.8

**Date:** 2019-09-13

Feature release

Added offer related attributes to article resource

## v3.1.7

**Date:** 2019-07-16

Feature release

### Features

Implemented external_reference filter for order

### Fixes

Doc Fix: Corrected some incorrectly documented fields from underscores to hypens. (created_at to created-at)
Doc Fix: Added missing uniqueness info to some resources


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


