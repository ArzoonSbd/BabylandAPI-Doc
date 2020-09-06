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
  "applied_delivery_class": 0,
  "products": [
    {
      "product_id": 187,
      "product": "http://dev.babylandworld.com/apps/product/electronic-bike/",
      "product_name": "electronic bike",
      "product_slug": "electronic-bike",
      "product_image": "http://dev.babylandworld.com/media/products/images/sc600x600.jpg",
      "product_stock_amount": 65,
      "product_price_unit": "Nrs.",
      "unit_cost": 770.0,
      "discount_percent": 5.0,
      "unit_final_cost": 731.5,
      "quantity": 5,
      "total_cost": 3657.5,
      "total_saved": 192.5
    }
  ],
  "discounted_amount": 192.5,
  "tax_amount": 332.5,
  "total": 3657.5
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
