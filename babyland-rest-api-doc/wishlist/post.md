[Back](../README.md)

# Create Wishlist

The post method api is used to add wishlist with valid customer login. To create new wishlist user should send valid product id in response body with array format.

**URL** : `/apps/wishlist/`

**Method** : `POST`

**Auth required** : YES

## Success Response

**Code** : `201 Created`

## Error Response

**Code** : `400 Bad Request`

**Reason** : `If invalid product id is added`

**Response** :

```json
{
    "detail": "Product not found"
}

Example :

{
   "products":["120"]
}
```

**JSON representation**

```json
{
  "product_id": "integer"
}
```

**Content examples**

```json
{
  "products": ["17", "19"]
}
```

**Parameters**
| Field | Type | Description |
| ------------------------------------------------------- | ----------- | ---------------------- |
| product_id `(required)` | integer | valid product id in array |

[Back](../README.md)
