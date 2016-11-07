# Group Properties

## List Properties [/properties]
Query list of properties

### By Address & Postcode [GET /properties{?address,postcode,page}]
Query with address (house number) and postcode

+ Parameters
    + address: `Flat 9` (required, string) - Property's address
    + postcode: `IP19 0NS` (required, string) - Property's UK postcode
    + page: `1` (optional, string) - Pagination meta

### By Postcode & Radius [GET /properties/area{?postcode,radius,page}]
Get a single note.

+ Parameters
    + postcode: `IP19 0NS` (required, string) - Property's UK postcode
    + page: `1` (optional, string) - Pagination meta