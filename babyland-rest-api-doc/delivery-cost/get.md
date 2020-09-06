[Back](../README.md)

# Get Delivery Cost List

Get list of all Delivery Cost.

**URL** : `/apps/delivery-cost/`

**Method** : `GET`

**Auth required** : Yes

## Success Response

**Code** : `200 OK`

**Response**

```json
{
  "id": 10,
  "price_class_a": 0.0,
  "price_class_b": 0.0,
  "price_class_c": 0.0,
  "district_name": "Panchthar",
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

[Back](../README.md)
