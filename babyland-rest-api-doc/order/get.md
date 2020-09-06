[Back](../README.md)

# Get Order List

Get list of all order.

**URL** : `/apps/order/all/`

**Method** : `GET`

**Auth required** : Yes

## Success Response

**Code** : `200 OK`

**Response**

```json
{
  "id": 1,
  "cart": {
    "no_of_items": 1,
    "products": [
      {
        "id": 6,
        "product_id": 174,
        "product": "http://dev.babylandworld.com/apps/product/fantastic-soft-shirt/",
        "p_name": "Fantastic Soft Shirt",
        "p_short_description": "Auto - FsbVAzZm",
        "p_price_unit": "Nrs.",
        "p_delivery_class": 2,
        "unit_cost": 433.23,
        "discount_percent": 0.0,
        "unit_final_cost": 433.23,
        "quantity": 10,
        "total_cost": 4332.3,
        "total_saved": 0.0
      }
    ],
    "discounted_amount": 0.0,
    "tax_amount": 0.0,
    "total": 4332.3
  },
  "final_cost": 4342.3,
  "payment_status": 0,
  "payment_method": 0,
  "order_status": 0,
  "delivery_status": 0,
  "code": "954bf518590d9",
  "name": "test_user",
  "addressline": "qwer43",
  "street": "qwe34",
  "city": "pokhara",
  "district": "Baglung",
  "phone": "string",
  "email": "user@example.com",
  "country": "string",
  "order_date": "2020-08-27T20:32:52.964000+02:00",
  "shipping_date": null,
  "delivery_date": null,
  "payment_date": null,
  "delivery_class": 2,
  "shipping_cost": 10.0,
  "c_email": "user@example.com",
  "c_name": "string",
  "customer": 207
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
