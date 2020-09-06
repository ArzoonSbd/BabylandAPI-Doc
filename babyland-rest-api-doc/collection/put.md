[Back](../README.md)

# Update Collection

This API is used to update collection of product with slug.

**URL** : `/apps/collection/{slug}/`

**Method** : `PUT`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

**Response**

```json
{
  "id": 3,
  "products": [187],
  "name": "latest vehicle",
  "slug": "vehicals",
  "image": "http://dev.babylandworld.com/media/collections/defaultImage.png"
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

Example :

```json
{
  "name": ["This field is required."]
}
```

**JSON representation of Content**

```json
{
  "products": "integer",
  "name": "string"
}
```

**Content examples**

```json
{
  "products": [187],
  "name": "latest vehicle"
}
```

**Parameters**
| Field | Type | Description |
| ------------------------------------------------------- | ----------- | ---------------------- |
| products `(required)` | integer | products id|
| name `(required)` | string | product name |
| slug `(readOnly and pattern: ^[-a-zA-Z0-9_]+$)`| string | product slug |
| image `(readonly)` | uri | product image |

[Back](../README.md)
