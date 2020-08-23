[Back](../README.md)

# Get Wishlist

Get Wishlist list if login with valid customer credential.

**URL** : `/apps/wishlist/`

**Method** : `GET`

**Auth required** : Yes

## Success Response

**Code** : `200 OK`

**Response**

```json
{
  "products": ["http://dev.babylandworld.com/apps/product/remote-car/"]
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
