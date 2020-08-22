[Back](../README.md)

# Add to Cart

To add products inside cart valid customer login is reguired and it accept bulk data in an array.

**URL** : `/apps/cart/`

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
  "id": "integer",
  "quantity": "integer"
}
```

**Content examples**

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

**Parameters**
| Field | Type | Description |
| ------------------------------------------------------- | ----------- | ---------------------- |
| id `(required)` | integer | valid product id in an array format|
| quantity`(optional)` | integer | products quantity|

[Back](../README.md)
