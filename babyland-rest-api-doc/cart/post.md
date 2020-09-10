[Back](../README.md)

# Add to Cart

To add products inside cart valid customer login is reguired and it accept bulk data in an array format.

**URL** : `/apps/cart/`

**Method** : `POST`

**Auth required** : YES

## Success Response

**Code** : `201 Created`

**Response**

```json
{
  "no_of_items": 1,
  "products": [
    {
      "product_id": 165,
      "product": "http://dev.babylandworld.com/apps/product/remote-car/",
      "unit_cost": 1000.0,
      "discount_percent": 10.0,
      "unit_final_cost": 900.0,
      "quantity": 1,
      "total_cost": 900.0,
      "total_saved": 100.0
    }
  ],
  "discounted_amount": 100.0,
  "tax_amount": 0.0,
  "total": 900.0
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

**Code** : `400 Bad Request`

**Reason** : `If invalid product id is added`

**Response** :

```json
{
  "detail": "Product not found"
}
```

**JSON representation of Content**

```json
{
  "products": [
    {
      "id": "integer",
      "quantity": "integer"
    }
  ]
}
```

**Content examples**

```json
{
  "products": [{ "id": "165", "quantity": "10" }]
}
```

**Parameters**

| Field           | Type    | Description                         |
| --------------- | ------- | ----------------------------------- |
| id `(required)` | integer | valid product id in an array format |
| quantity        | integer | products quantity                   |

[Back](../README.md)
