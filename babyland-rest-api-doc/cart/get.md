[Back](../README.md)

# Get Cart

Get cart details list if login with valid customer credential. If there is no any cart then initial value is as 0.

**URL** : `/apps/cart/`

**Method** : `GET`

**Auth required** : Yes

## Success Response

**Code** : `200 OK`

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

[Back](../README.md)
