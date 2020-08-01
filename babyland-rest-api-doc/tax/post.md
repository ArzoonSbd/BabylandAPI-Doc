[Back](../README.md)

# Create New Tax

To create a category.

**URL** : `/apps/tax/`

**Method** : `POST`

**Auth required** : YES

## Success Response

**Code** : `201 Created`

## Error Response

**Code** : `404 Not Found`

**Reason** : `No tax with the id found`

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
  "percent": "number"
}
```

**Content examples**

```json
{
  "id": 37,
  "url": "http://dev.babylandworld.com/apps/tax/37/",
  "name": "zero tax",
  "percent": 0.0
}
```

**Parameters**
| Field | Type | Description |
| ------------------------------------------------------- | ----------- | ---------------------- |
| name `(required and [1 .. 255 ] characters)`| string | tax name |
| percent | number | tax percent |

[Back](../README.md)
