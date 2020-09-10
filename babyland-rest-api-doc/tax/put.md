[Back](../README.md)

# Update Tax By ID

Change whole content of a tax with given id.

**URL** : `/apps/tax/{id}/`

**Method** : `PUT`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

**Content examples**

```json
{
  "id": 37,
  "url": "http://dev.babylandworld.com/apps/tax/37/",
  "name": "zero tax",
  "percent": 20.0
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

Example :

{
    "name": [
        "Ensure this field has no more than 255 characters."
    ]
}
```

**JSON representation of content**

```json
{
  "name": "string",
  "percent": "number"
}
```

**Parameters**

| Field                                        | Type   | Description |
| -------------------------------------------- | ------ | ----------- |
| name `(required and [1 .. 255 ] characters)` | string | tax name    |
| percent `(from 1 to 100 %)`                  | number | tax percent |

[Back](../README.md)
