[Back](../README.md)

# Delete Wishlist

To delete wishlist valid customer token is required and send products id in json body.

**URL** : `/apps/wishlist/`

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

**JSON representation of content**

```json
{
  "product": { "id": "integer" }
}
```

**Content examples**

```json
{
  "products": "164"
}
```

**Parameters**
| Field | Type | Description |
| ------------------------------------------------------- | ----------- | ---------------------- |
| id `(required)` | integer | product id to delete from wishlist|

[Back](../README.md)
