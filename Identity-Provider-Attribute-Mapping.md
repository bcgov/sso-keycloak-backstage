Attribute mapping for IDIR and BCeID:

| KeyCloak                          |
|---                                |
| `idir_userid` or `bceid_userid`   |
| username                          |
| email                             |
| displayName                       |

Additional Attributes available with IDIR only

| KeyCloak                          |
|---                                |
| firstName                         |
| lastName                          |

Additional Attributes available with standard Business BCeID

| KeyCloak                          |
|---                                |
| bceid_business_name               |
| bceid_business_guid               |


* User's `First Name` and `Last Name` are NOT available for BCeID users.
* Developers should ONLY use the attributes in the `KeyCloak` column.
* Any other attribute can be fetched by the app itself using [IDIM Web Services](https://sminfo.gov.bc.ca/)