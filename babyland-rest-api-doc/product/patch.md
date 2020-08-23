[Back](../README.md)

# Partial Update Product By Slug

Update the partial fields of product with given slug.

**URL** : `/apps/product/{slug}/`

**Method** : `PATCH`

**Auth required** : YES

## Success Response

**Code** : `200 OK`

**Response** :

```json
{
  "id": 2,
  "url": "http://dev.babylandworld.com/apps/product/handmade-soft-car/",
  "active": false,
  "slug": "handmade-soft-car",
  "sku": "Auto - mCkauKE2w4biXgM",
  "name": "Handmade Soft Car",
  "short_description": "Auto - 5J70mHij",
  "description": "Auto - O4MR1oRZ6XsaStx",
  "creation_date": "2020-08-23T13:41:08.278095+02:00",
  "deliverable": false,
  "stock_amount": 1.0,
  "stock_unit": "70",
  "weight": null,
  "weight_unit": "",
  "height": 70.0,
  "height_unit": "",
  "length": null,
  "length_unit": "",
  "width": null,
  "width_unit": "",
  "tax_type": null,
  "manufacturer": "France",
  "active_sku": false,
  "active_short_description": false,
  "active_dimension": false,
  "active_weight": false,
  "specification": {},
  "primary_category": "http://dev.babylandworld.com/apps/category/cheese/",
  "images": [],
  "price": 445.41,
  "initial_cost": 445,
  "has_discount": true,
  "discount_percent": 70.0,
  "final_cost": 133,
  "price_unit": "Nepalese Rupee"
}
```

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

**JSON representation of content**

```json
{
  "name": "string",
  "price": "number",
  "discount_percent": "number",
  "short_description": "string",
  "description": "string",
  "stock_amount": "number",
  "stock_unit": "string",
  "weight": "number",
  "weight_unit": "string",
  "height": "number",
  "height_unit": "string",
  "length": "number",
  "length_unit": "string",
  "width": "number",
  "width_unit": "string",
  "tax_type": "string",
  "manufacturer": "string",
  "active_weight": "boolean",
  "specification": "object",
  "primary_category": "string"
}
```

**Content examples**

```json
{
  "slug": "handmade-soft-car",
  "sku": "Auto - mCkauKE2w4biXgM",
  "name": "Handmade Soft Car",
  "short_description": "Auto - 5J70mHij",
  "description": "Auto - O4MR1oRZ6XsaStx",
  "stock_amount": 1.0,
  "stock_unit": "70",
  "height": 70.0,
  "manufacturer": "France",
  "primary_category": "http://dev.babylandworld.com/apps/category/cheese/",
  "price": 445.41,
  "initial_cost": 445,
  "has_discount": true,
  "discount_percent": 70.0
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
