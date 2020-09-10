[Back](../README.md)

# Create Wishlist

The post method api is used to add wishlist with valid customer login. To create new wishlist user should send valid product id in response body with array format.

**URL** : `/apps/wishlist/`

**Method** : `POST`

**Auth required** : YES

## Success Response

**Code** : `201 Created`

**Response**

```json
{
  "products": [
    "http://dev.babylandworld.com/apps/product/incredible-steel-mouse/"
  ]
}
```

## Error Response

**Code** : `400 Bad Request`

**Reason** : `If invalid product id is added`

**Response** :

```json
{
  "detail": "Product not found"
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
  "products": ["1"]
}
```

**Parameters**

| Field                   | Type    | Description                         |
| ----------------------- | ------- | ----------------------------------- |
| product_id `(required)` | integer | valid product id to add in wishlist |

[Back](../README.md)
