[Back](../README.md)

# Create Order

To create a product order.

**URL** : `/apps/order/`

**Method** : `POST`

**Auth required** : YES

## Success Response

**Code** : `201 Created`

**Response** :

```json
{
  "id": 6,
  "final_cost": 1486.9,
  "payment_status": 0,
  "payment_method": 0,
  "order_status": 0,
  "delivery_status": 0,
  "code": "bad2d803aceb26",
  "name": "test_user",
  "addressline": "qwer43",
  "street": "qwe34",
  "city": "pokhara",
  "district": "Baglung",
  "phone": "987654321",
  "email": "user@example.com",
  "country": "Nepal",
  "order_date": "2020-09-02T17:24:30.984695+02:00",
  "shipping_date": null,
  "delivery_date": null,
  "payment_date": null,
  "delivery_class": 2,
  "shipping_cost": 10.0,
  "c_email": "user@example.com",
  "c_name": "345wert",
  "customer": 207,
  "cart": 11
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
  "payment_status": 0,
  "payment_method": 0,
  "order_status": 0,
  "delivery_status": 0,
  "name": "test_user",
  "addressline": "qwer43",
  "street": "qwe34",
  "city": "pokhara",
  "phone": "987654321",
  "email": "user@example.com",
  "country": "Nepal",
  "delivery_class": 0,
  "shipping_cost": 0,
  "c_email": "user@example.com",
  "c_name": "345wert",
  "customer": "wert",
  "cart": 0
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
