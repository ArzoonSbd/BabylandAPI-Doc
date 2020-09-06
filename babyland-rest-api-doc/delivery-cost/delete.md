[Back](../README.md)

# Delete Delivery Cost by ID

Only valid staff have permission to delete delivery cost along with ID.

**URL** : `/apps/delivery-cost/{id}/`

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

**Code** : `403 Forbidden`

**Reason** : `If customer token provided in header`

**Response** :

```json
{
  "detail": "You do not have permission to perform this action."
}
```

[Back](../README.md)
