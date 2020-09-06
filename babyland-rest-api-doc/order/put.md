[Back](../README.md)

# Update Order by ID

Update a product order by id from valid staff token.

**URL** : `/apps/order/{id}/`

**Method** : `PUT`

**Auth required** : YES

## Success Response

**Code** : `200 Ok`

**Response** :

```json
{
  "id": 12,
  "cart": {
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
  },
  "final_cost": 3465.0,
  "payment_status": 1,
  "payment_method": 0,
  "order_status": 0,
  "delivery_status": 1,
  "code": "1d07e3229370fe6",
  "name": "test@user",
  "addressline": "add-1234",
  "street": "25",
  "city": "Kathmandu",
  "district": "Baglung",
  "phone": "987654321",
  "email": "test@user.com",
  "country": "Nepal",
  "order_date": "2020-09-05T15:33:14.770166+02:00",
  "shipping_date": "2020-09-05T14:21:48+02:00",
  "delivery_date": null,
  "payment_date": "2020-09-05T13:33:14+02:00",
  "delivery_class": 0,
  "shipping_cost": 0.0,
  "c_email": "test@example.com",
  "c_name": "345wert",
  "customer": 207
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
  "name": "string",
  "addressline": "string",
  "street": "string",
  "city": "string",
  "district": "string",
  "phone": "string",
  "email": "string",
  "country": "string",
  "delivery_class": "integer",
  "shipping_cost": "number",
  "c_email": "string",
  "c_name": "string",
  "customer": "string",
  "cart": "integer"
}
```

**Content examples**

```json
{
  "id": 12,
  "cart": {
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
  },
  "final_cost": 3465.0,
  "payment_status": 1,
  "payment_method": 0,
  "order_status": 0,
  "delivery_status": 1,
  "code": "1d07e3229370fe6",
  "name": "test@user",
  "addressline": "add-1234",
  "street": "25",
  "city": "Kathmandu",
  "district": "Baglung",
  "phone": "987654321",
  "email": "test@user.com",
  "country": "Nepal",
  "delivery_date": null,
  "delivery_class": 0,
  "shipping_cost": 0.0,
  "c_email": "test@example.com",
  "c_name": "345wert",
  "customer": 207
}
```

**Parameters**
| Field | Type | Description |
| ------------------------------------------------------- | ----------- | ---------------------- |
| final_cost `(read only)` | number | product final cost |
| payment_status `(Enum:[0,1])` | integer | order payment status |
| payment_method `(Enum:[0])` | string | order payment method|
| order_status `( Enum:[0,1,2,3,4])` | integer | order status |
| delivery_status `(Enum:[0,1,2])`| integer | order delivery status |
| code `(read only)`| string | order code|
| name `(required and maxlength:100)`| string | customer name |
| addressline `( optional and [1 .. 100] characters)` | string | customer addressline |
| street `(required and [1 .. 250] characters)` | string | customer street |
| city `(required and [1..50] characters)` | string | customer city address |
| district `(required and Enum)`| string | all 77 district |
| phone `(maxlength:20)`| string | customer phone |
| email `(required and [ 1 .. 255 ] characters)` | string | email address |
| country | string | country name |
| order_date `(default date now)`| date-time | order date|
| shipping_date `(default date now)`| date-time | shipping date|
| delivery_date `(default date now)`| date-time | delivery date|
| payment_date `(default date now)`| date-time | payment date|
| delivery_class| integer | delivery class |
| shipping_cost| number | shipping cost |
| c_email `(maxlength:254 character)`| string | customer email |
| c_name `(maxlength:180 character)`| string | customer name |
| cart `(required)`| integer | cart |

[Back](../README.md)
