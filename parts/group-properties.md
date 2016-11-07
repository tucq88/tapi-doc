# Group Properties

## List Properties [/properties]
Query list of properties

### By Address & Postcode [GET /properties{?address,postcode,page}]
Query with address (house number) and postcode

+ Parameters
    + address: `Flat 9` (required, string) - Property's address
    + postcode: `324A-B234` (required, string) - Property's postcode
    + page: `1` (optional, string) - Pagination meta

<!-- ### By Postcode & Radius [GET /properties/area{?postcode,radius,page}]
Get a single note.

+ Parameters
    + postcode: `324A-B234` (required, string) - Full property's postcode
    + radius: `10` (optional, string) - Radius with center is property's postcode
        + Members
            + 10
            + 20
            + 30
            + 50
    + page: `1` (optional, string) - Pagination meta -->