[Back](../README.md)

# Get Wishlist

Get Wishlist list if login with valid customer credential.

**URL** : `/apps/wishlist/`

**Method** : `GET`

**Auth required** : Yes

## Success Response

**Code** : `200 OK`

**JSON representation of success response**

```json
{
  "products": "Array of strings"
}
```

**Content examples**

```json
{
  "products": ["http://dev.babylandworld.com/apps/product/remote-car/"]
}
```

[Back](../README.md)
