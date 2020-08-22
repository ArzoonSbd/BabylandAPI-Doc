[Back](../README.md)

# Update Category By Slug

Change whole content of a category with given slug.

**URL** : `/apps/category/{slug}/`

**Method** : `PUT`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

## Error Response

**Code** : `404 Not Found`

**Reason** : `No category with the slug found`

**Response** :

```json
{
  "detail": "Not found."
}
```

**Code** : `400 Bad Request`

**Reason** : `Field validation error`

**Response** :

```json
{
    "<fieldname>": "[<Validation Error>]"
}

Example :

{
    "name": [
        "Ensure this field has no more than 100 characters."
    ]
}
```

**JSON representation**

```json
{
  "id": "integer",
  "url": "string",
  "name": "string",
  "level": "integer",
  "parent": "string",
  "specification": "object",
  "products": "Array of strings"
}
```

**Content examples**

```json
{
  "id": 192,
  "url": "http://dev.babylandworld.com/apps/category/computer/",
  "name": "Computer",
  "level": 0,
  "parent": null,
  "specification": [
    {
      "id": 0,
      "name": "Ram ",
      "type": "selection",
      "default": "4 GB",
      "options": ["8 GB", "4 GB"]
    },
    {
      "id": 1,
      "name": "Processor",
      "type": "selection",
      "default": "I3",
      "options": ["I5", "I3", "I7"]
    }
  ],
  "children": [193, 194],
  "slug": "computer",
  "image": "http://dev.babylandworld.com/media/category/images/cover_letter_of.com.np.jpg"
}
```

**Parameters**

Every fields below must be supplied.

| Field                                                   | Type        | Description            |
| ------------------------------------------------------- | ----------- | ---------------------- |
| name `(required and [ 1 .. 100 ] characters)`           | string      | category name          |
| level `(required and [ 0 .. 32767 ])`                   | integer     | category level         |
| parent `(required if level isnot 0)`                    | uri-string  | parent category        |
| specification `(not null - minimum null JSON required)` | json object | category specification |

[Back](../README.md)
