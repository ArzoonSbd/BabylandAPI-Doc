[Back](../README.md)

# Create Category

To create a category.

**URL** : `/apps/category/`

**Method** : `POST`

**Auth required** : YES

## Success Response

**Code** : `201 Created`

**Response** :

```json
{
  "id": 18,
  "url": "http://dev.babylandworld.com/apps/category/laptop/",
  "name": "Laptop",
  "level": 1,
  "parent": 17,
  "specification": [
    {
      "name": "Ram ",
      "type": "selection",
      "default": "4 GB",
      "options": ["8 GB", "4 GB"]
    },
    {
      "name": "Processor",
      "type": "selection",
      "default": "I3",
      "options": ["I5", "I3", "I7"]
    }
  ],
  "children": [],
  "slug": "laptop",
  "image": "http://dev.babylandworld.com/media/category/images/cover_letter_of.com.np.jpg"
}
```

## Error Response

**Code** : `401 Unauthorized`

**Reason** : `No authentication token provided in header`

**Response** :

```json
{
  "detail": "Authentication credentials were not provided."
}
```

**Code** : `400 Bad Request`

**Reason** : `Field validation error`

**Response** :

```json
{
  "<fieldname>": "[<Validation Error>]"
}
```

```json
Example :

{
    "name": [
        "Ensure this field has no more than 100 characters."
    ]
}
```

**JSON representation of Content**

```json
{
  "name": "String",
  "level": "Level_number",
  "parent": "Id_number",
  "specification": "JSON Object",
  "image": "Image File"
}
```

**Content examples**

```json
{
  "name": "Laptop",
  "level": "1",
  "parent": "17",
  "specification": [
    {
      "name": "Ram ",
      "type": "selection",
      "default": "4 GB",
      "options": ["8 GB", "4 GB"]
    },
    {
      "name": "Processor",
      "type": "selection",
      "default": "I3",
      "options": ["I5", "I3", "I7"]
    }
  ]
}
```

**Parameters**

| Field                                                   | Type        | Description            |
| ------------------------------------------------------- | ----------- | ---------------------- |
| name `(required and [ 1 .. 100 ] characters)`           | string      | category name          |
| level `(required and [ 0 .. 32767 ])`                   | integer     | category level         |
| parent `(required if level isnot 0)`                    | integer     | parent category        |
| specification `(not null - minimum null JSON required)` | json object | category specification |
| image                                                   | Image file  | Image for the category |

[Back](../README.md)