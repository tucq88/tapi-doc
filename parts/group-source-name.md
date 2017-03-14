# Group Source Name

### Get Name [GET /sourcename/get-name{?uprn,showAll,usage}]
Get name by using `UPRN` as param. By default, only return primary contact records.

+ Parameters
    + uprn: `10003932392` (required, string) - URPN value
    + showAll: `false` (optional, string) -
        + Set `false` by default as only display primary contact records
        + Use `true` if you want to get all records
    + usage: `single` (required, string) - Default value is `single`
