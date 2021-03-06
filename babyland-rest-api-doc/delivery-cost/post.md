[Back](../README.md)

# Create Delivery Cost

This API is used to create delivery cost along with price details and district area.

**URL** : `/apps/delivery-cost/`

**Method** : `POST`

**Auth required** : YES

## Success Response

**Code** : `201 Created`

**Response**

```json
{
  "id": 17,
  "price_class_a": 300.0,
  "price_class_b": 0.0,
  "price_class_c": 0.0,
  "district_name": "Palpa",
  "price_unit": "Nrs."
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
  "district_name": ["This field is required."]
}
```

**JSON representation of Content**

```json
{
  "price_class_a": "number",
  "price_class_b": "number",
  "price_class_c": "number",
  "district_name": "string",
  "price_unit": "string"
}
```

**Content examples**

```json
{
  "id": 17,
  "price_class_a": 300.0,
  "price_class_b": 0.0,
  "price_class_c": 0.0,
  "district_name": "Palpa",
  "price_unit": "Nrs."
}
```

**Parameters**

| Field                               | Type   | Description                 |
| ----------------------------------- | ------ | --------------------------- |
| price_class_a `(required)`          | number | class a item category price |
| price_class_b `(required)`          | number | class b item category price |
| price_class_c `(required)`          | number | class c item category price |
| district_name `(required and enum)` | string | 77 district name            |
| price_unit `(enum:[ Nrs., $ ])`     | string | item price unit             |

[Back](../README.md)
