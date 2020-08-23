[Back](../README.md)

# Delete Wishlist

Customer is only able to delete specific wishlist.

**URL** : `/api/user/`

**Method** : `DELETE`

**Auth required** : YES

## Success Response

**Code** : `204`

## Error Response

**Code** : `400 Bad Request`

**Response**:

```json
{
  "detail": "Product to delete is required"
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
