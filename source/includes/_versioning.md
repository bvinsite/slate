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

For example, when version 3.2.12 is the latest published API version, the API versions are available at the following URIs:


| Base Path     | API Version  |
| ------------- |:--------------|
| /api/v3       | v.3.2.12      |
| /api/v31      | v.3.1.x       |
| /api/v32      | v.3.2.12      |

