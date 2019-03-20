_release_history.md
# Release History

## v3.0.0

### v3.0.5

**Date:** 2018-11-07

First public release of the v3 API

### v3.0.6

**Date:** 2018-12-06

Feature/ bugfix release

### Features

- Adds delivery_at / targeted_at filters to

## v3.1.0

**Date:** 2019-03-20

Feature release

### Compatibility

 - Paginated responses are _only_ allowed to user either number/size for paged pagination, or offset/limit for offset pagination

### Features

Implemented a Paged Paginator. The paginator can be selected in the request by including

- page[offset] and page[limit] parameters, or
- page[number] and page[size] parameters
