[Back](../README.md)

# Create Category

To create a category.

**URL** : `/apps/category/`

**Method** : `POST`

**Auth required** : YES

## Success Response

**Code** : `201 Created`

## Error Response

**Code** : `404 Not Found`

**Reason** : `No category with the id found`

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
  "id": 118,
  "url": "http://dev.babylandworld.com/apps/category/118/",
  "name": "Dell Laptop",
  "level": 1,
  "parent": "http://dev.babylandworld.com/apps/category/117/",
  "specification": [
    {
      "id": 0,
      "name": "Ram",
      "type": "selection",
      "default": "",
      "options": ["2gb"]
    },
    {
      "id": 1,
      "name": "Core Processor",
      "type": "text",
      "default": "i3"
    },
    {
      "id": 2,
      "name": "Keyboard",
      "type": "number",
      "default": "2pcs"
    }
  ],
  "products": ["http://dev.babylandworld.com/apps/product/109/"]
}
```

**Parameters**

| Field                                                   | Type        | Description            |
| ------------------------------------------------------- | ----------- | ---------------------- |
| name `(required and [ 1 .. 100 ] characters)`           | string      | category name          |
| level `(required and [ 0 .. 32767 ])`                   | integer     | category level         |
| parent `(required if level isnot 0)`                    | uri-string  | parent category        |
| specification `(not null - minimum null JSON required)` | json object | category specification |

[Back](../README.md)
