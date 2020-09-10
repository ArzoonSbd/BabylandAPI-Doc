[Back](../README.md)

# Create Delivery Cost

This API is used to partial update delivery cost along with price details and district area.

**URL** : `/apps/delivery-cost/{id}/`

**Method** : `PATCH`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

**Response**

```json
{
  "id": 19,
  "price_class_a": 1000.0,
  "price_class_b": 0.0,
  "price_class_c": 0.0,
  "district_name": "Bajura",
  "price_unit": "$"
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

**JSON representation of Content**

```json
{
  "price_class_a": "number",
  "price_unit": "string"
}
```

**Content examples**

```json
{
  "price_unit": "$",
  "price_class_a": 1000
}
```

**Parameters**

| Field                               | Type   | Description                 |
| ----------------------------------- | ------ | --------------------------- |
| price_class_a `(required)`          | number | class a item category price |
| price_class_b `(required)`          | number | class b item category price |
| price_class_c `(required)`          | number | class c item category price |
| district_name `(required and enum)` | string | 77 district name            |
