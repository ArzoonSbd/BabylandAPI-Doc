[Back](../README.md)

# Get Tax List

Get list of all tax.

**URL** : `/apps/tax/`

**Method** : `GET`

**Auth required** : Yes

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

[Back](../README.md)
