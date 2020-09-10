[Back](../README.md)

# Update Order by ID and cart

Update a product order by id and cart from valid staff token.

**URL** : `/apps/order/{id}/cart/`

**Method** : `PUT`

**Auth required** : YES

## Success Response

**Code** : `200 Ok`

**Response** :

```json
{
  "no_of_items": 1,
  "products": [
    {
      "id": 23,
      "product_id": 187,
      "product": "http://dev.babylandworld.com/apps/product/electronic-bike/",
      "p_name": "electronic bike",
      "p_short_description": "electronic bike",
      "p_price_unit": "Nrs.",
      "p_delivery_class": 0,
      "unit_cost": 770.0,
      "discount_percent": 10.0,
      "unit_final_cost": 693.0,
      "quantity": 5,
      "total_cost": 3465.0,
      "total_saved": 385.0
    }
  ],
  "discounted_amount": 385.0,
  "tax_amount": 63.0,
  "total": 3465.0
}
```

## Error Response

**Code** : `400 Bad Request`

**Reason** : `Field validation error`

**Response** :

```json
{
  "<fieldname>": "[<Validation Error>]"
}
```

Example :

```json
{
  "name": ["Ensure this field has no more than 100 characters."]
}
```

**Code** : `403 Forbidden`

**Reason** : `Customer login token`

**Response** :

```json
{
  "detail": "You do not have permission to perform this action."
}
```

**JSON representation of content**

```json
{
  "product": "string",
  "p_name": "string",
  "p_short_description": "string",
  "p_price_unit": "string",
  "p_delivery_class": "integer",
  "quantity": "integer"
}
```

**Content examples**

```json
{
  "no_of_items": 1,
  "products": [
    {
      "id": 23,
      "product_id": 187,
      "product": "http://dev.babylandworld.com/apps/product/electronic-bike/",
      "p_name": "electronic bike",
      "p_short_description": "electronic bike",
      "p_price_unit": "Nrs.",
      "p_delivery_class": 0,
      "unit_cost": 770.0,
      "discount_percent": 10.0,
      "unit_final_cost": 693.0,
      "quantity": 5,
      "total_cost": 3465.0,
      "total_saved": 385.0
    }
  ],
  "discounted_amount": 385.0,
  "tax_amount": 63.0,
  "total": 3465.0
}
```

**Parameters**

| Field               | Type    | Description               |
| ------------------- | ------- | ------------------------- |
| product             | string  | product url               |
| p_name              | string  | product name              |
| p_short_description | string  | product short description |
| p_price_unit        | string  | product price unit        |
| p_delivery_class    | integer | product delivery class    |
| quantity            | integer | product quantity          |

[Back](../README.md)
