# Group Authentication

## User Login [POST /user/login]
Query list of properties

#### Request Attributes
Name | Contrains | Description
---- | --------- | -----------
email  | `email`  `required` | User unique email
password  | `string`  `required` | User secret password

+ Request Sample
    {
        "email": "user@example.com",
        "password": "123456",
    }
