[Back](../README.md)

# Delete Product By Slug

**URL** : `/apps/product/{slug}/`

**Method** : `DELETE`

**Auth required** : YES

## Success Response

**Code** : `204`

## Error Response

**Code** : `404 Not Found`

**Response**:

```json
{
  "detail": "Not found."
}
```

**Code** : `401 Unauthorized`

**Reason** : `No authentication token provided in header`

**Response** :

```json
{
  "detail": "Authentication credentials were not provided."
}
```

[Back](../README.md)
