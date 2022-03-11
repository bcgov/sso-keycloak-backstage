Attribute mapping for IDIR and BCeID:

| LDAP (IDIR-only)| SAML            | KeyCloak                          |
|---              |---              |---                                |
| bcgovGUID       | useridentifier  | `idir_userid` or `bceid_userid`   |
| samaccountname  | username        | username                          |
| mail            | email           | email                             |
| displayName     | displayName     | displayName                       |

Additional Attributes available with IDIR only

| givenName       | firstName       | firstName                         |
| sn              | lastName        | lastName                          |

Additional Attributes available with standard Business BCeID

| KeyCloak                          |
|---                                |
| bceid_business_name               |
| bceid_business_guid               |


* User's `First Name` and `Last Name` are NOT available for BCeID users.
* Developers should ONLY use the attributes in the `KeyCloak` column.
* Any other attribute can be fetched by the app itself using [IDIM Web Services](https://sminfo.gov.bc.ca/)