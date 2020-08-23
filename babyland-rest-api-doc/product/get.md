[Back](../README.md)

# Get Product List

Get list of all product.

**URL** : `/apps/product/`

**Method** : `GET`

**Auth required** : Yes

## Success Response

**Code** : `200 OK`

**Response**

```json
{
  "id": 1,
  "url": "http://dev.babylandworld.com/apps/product/incredible-steel-mouse/",
  "active": false,
  "slug": "incredible-steel-mouse",
  "sku": "Auto - 0A9CG2Wp5ddjCoI",
  "name": "Incredible Steel Mouse",
  "short_description": "Auto - 4zGaMeCT",
  "description": "Auto - KKmhal1VKME9XMb",
  "creation_date": "2020-08-22T15:41:21.341143+02:00",
  "deliverable": false,
  "stock_amount": 1.0,
  "stock_unit": "68",
  "weight": null,
  "weight_unit": "",
  "height": 68.0,
  "height_unit": "",
  "length": null,
  "length_unit": "",
  "width": null,
  "width_unit": "",
  "tax_type": null,
  "manufacturer": "Mali",
  "active_sku": false,
  "active_short_description": false,
  "active_dimension": false,
  "active_weight": false,
  "specification": {},
  "primary_category": "http://dev.babylandworld.com/apps/category/pizza/",
  "images": [],
  "price": 4.06,
  "initial_cost": 4,
  "has_discount": true,
  "discount_percent": 68.0,
  "final_cost": 1,
  "price_unit": "Nepalese Rupee"
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