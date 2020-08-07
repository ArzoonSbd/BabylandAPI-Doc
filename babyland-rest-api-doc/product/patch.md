[Back](../README.md)

# Partial Update Product By ID

Update the partial fields of product with given id.

**URL** : `/apps/product/{id}/`

**Method** : `PATCH`

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
  "id": "integer",
  "url": "string",
  "active": "boolean",
  "slug": "string",
  "sku": "string",
  "name": "string",
  "price": "number",
  "discount_percent": "number",
  "price_unit": "string",
  "short_description": "string",
  "description": "string",
  "for_sale": "boolean",
  "for_sale_percent": "number",
  "for_sale_price": "number",
  "creation_date": "string",
  "deliverable": "boolean",
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
  "active_sku": "boolean",
  "active_short_description": "boolean",
  "active_description": "boolean",
  "active_dimension": "boolean",
  "specification": "object",
  "primary_category": "string",
  "images": "array of objects"
}
```

**Content examples**

```json
{
  "id": 107,
  "url": "http://dev.babylandworld.com/apps/product/107/",
  "active": true,
  "slug": "cars-for-kids",
  "sku": "kids-car-2020",
  "name": "kids car",
  "price": 2000.0,
  "discount_percent": 10.0,
  "price_unit": "Nepalese Rupee",
  "short_description": "cars for kids",
  "description": "this is cars for kids. Your kids wil be happy !!!hshhspii;hdbbcbbhhskjsj;fnnhdjhdkn;djsj",
  "creation_date": "2020-07-18T17:42:53.729223+02:00",
  "deliverable": true,
  "stock_amount": 20.0,
  "stock_unit": "piece",
  "weight": "",
  "weight_unit": "",
  "height": null,
  "height_unit": "",
  "length": null,
  "length_unit": "",
  "width": null,
  "width_unit": "",
  "tax_type": "http://dev.babylandworld.com/apps/tax/37/",
  "manufacturer": "tesla",
  "active_sku": true,
  "active_short_description": true,
  "active_description": true,
  "active_dimension": false,
  "active_weight": false,
  "specification": {
    "name": "tesla",
    "type": "kids",
    "model": "2020"
  },
  "primary_category": "http://dev.babylandworld.com/apps/category/121/",
  "images": [
    {
      "id": 88,
      "product": 107,
      "name": "cars",
      "image_file": "http://dev.babylandworld.com/media/products/logo.jpg"
    },
    {
      "id": 89,
      "product": 107,
      "name": "me",
      "image_file": "http://dev.babylandworld.com/media/products/es6.jpeg"
    }
  ]
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
