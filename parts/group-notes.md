# Data Structures

## NoteData
+ id: 1 (required, number) - Unique identifier
+ title: Grocery list (required) - Single line description
+ body: Buy milk - Full description of the note which supports Markdown.

## NoteList (array)
+ (NoteData)

# Group Notes
Group description (also with *Markdown*)

## Important Infooo
Descriptions may also contain sub-headings and **more Markdown**.

## Note List [/notes]
Note list description

+ Even
+ More
+ Markdown

### Get Notes [GET]
Get a list of notes.

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (NoteList)

### Create New Note [POST]
Create a new note using a title and an optional content body.

+ Request with body (application/json)

    + Body

            {
                "title": "My new note",
                "body": "This is the body"
            }

+ Response 201

+ Response 400 (application/json)

    + Body

            {
                "error": "Invalid title"
            }

+ Request without body (application/json)

    + Body

            {
                "title": "My new note"
            }

+ Response 201

+ Response 400 (application/json)

    + Body

            {
                "error": "Invalid title"
            }

## Note [/notes/{id}{?body}]
Note description

+ Parameters

    + id: `68a5sdf67` (required, string) - The note ID

### Get Note [GET]
Get a single note.

+ Parameters

    + body: `false` (boolean) - Set to `false` to exclude note body content.

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (NoteData)

+ Response 404 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Body

            {
                "error": "Note not found"
            }

### Update a Note [PUT]
Update a single note by setting the title and/or body.

::: warning
#### <i class="fa fa-warning"></i> Caution
If the value for `title` or `body` is `null` or `undefined`, then the corresponding value is not modified on the server. However, if you send an empty string instead then it will **permanently overwrite** the original value.
:::

+ Request (application/json)

    + Body

            {
                "title": "Grocery List (Safeway)"
            }

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (NoteData)

+ Response 404 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Body

            {
                "error": "Note not found"
            }

+ Request delete body (application/json)

    + Body

            {
                "body": ""
            }

+ Response 200 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Attributes (NoteData)

+ Response 404 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Body

            {
                "error": "Note not found"
            }

### Delete a Note [DELETE]
Delete a single note

+ Response 204

+ Response 404 (application/json)

    + Headers

            X-Request-ID: f72fc914
            X-Response-Time: 4ms

    + Body

            {
                "error": "Note not found"
            }