[Back](../README.md)

# Update Product By Slug

Change whole content of a product with given slug.

**URL** : `/apps/product/{slug}/`

**Method** : `PUT`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

## Error Response

**Code** : `404 Not Found`

**Reason** : `No product with the id found`

**Response** :

```json
{
  "detail": "Not found."
}
```

**Code** : `400 Bad Request`

**Reason** : `Field validation error`

**Response** :

```json
{
    "<fieldname>": "[<Validation Error>]"
}

Example :

{
    "name": [
        "Ensure this field has no more than 100 characters."
    ]
}
```

**JSON representation**

```json
{
  "price_unit": "Nepalese Rupee"
}
```

**Parameters**
| Field | Type | Description |
| ------------------------------------------------------- | ----------- | ---------------------- |
| active `(default true)` | boolean | product status |
| slug `(read only)` | string | product slug |
| sku `(required and [ 1 .. 255 ] characters)` | string | product sku |
| name `(required and [ 1 .. 255 ] characters)` | string | product name |
| price `(required)`| number | products price |
| discount_percent `(default 0)`| number | products discount percent |
| price_unit `(default Nrs.)`| string | products price unit |
| short_description `(required and [ 1 .. 1000 ] characters)` | string | products short description |
| description `(optional and [ 1 .. 8000 ] characters)` | string | products description |
| creation_date `(read only and default date now)` | date | products create date |
| deliverable `(default true)`| boolean | products deliverable |
| stock_amount `(default 1)`| number | products stock amount |
| stock_unit `(required and [ 1 .. 255 ] characters)` | string | products stock unit |
| weight | number | products weight |
| weight_unit `(max 255 characters)`| string | products weight unit |
| height | number | products height |
| height_unit `(max 255 characters)` | string | products height unit |
| width | number | products width |
| width_unit `(max 255 characters)`| string | products width unit |
| tax_type `(foreign key to product)`| string | products tax type |
| manufacturer `(required and [ 1 .. 255 ] characters)` | string | products manufacturer |
| active_sku `(default true)`| boolean | products active sku status |
| active_short_description `(default true)`| boolean | products active short description |
| active_description `(default true)`| boolean | products active description |
| active_dimension `(default false)` | boolean | products active dimension |
| active_weight `(default false)`| boolean | products active weight |
| specification `(not null - minimum null JSON required)` | json object | category specification |
| primary_category `(required and foreign key to category)` | string | products primary category |
| images | json array of objects | products images |

[Back](../README.md)
