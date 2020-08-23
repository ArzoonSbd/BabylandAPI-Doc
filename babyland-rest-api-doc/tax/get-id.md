[Back](../README.md)

# Get Tax By ID

Get detail of a tax with given id.

**URL** : `/apps/tax/{id}/`

**Method** : `GET`

**Auth required** : NO

## Success Response

**Code** : `200 OK`

**Response**

```json
{
  "id": 37,
  "url": "http://dev.babylandworld.com/apps/tax/37/",
  "name": "zero tax",
  "percent": 0.0
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

**Code** : `404 Not Found`

**JSON representation**

```json
{
  "detail": "Not found."
}
```

**Reason** : `Tax with the given id doesn't exist.`

[Back](../README.md)
