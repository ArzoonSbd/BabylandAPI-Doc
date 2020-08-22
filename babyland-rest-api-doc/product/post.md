[Back](../README.md)

# Create Product

To create a product.

**URL** : `/apps/product/`

**Method** : `POST`

**Auth required** : YES

## Success Response

**Code** : `201 Created`

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
  "active_weight": "boolean",
  "specification": "object",
  "primary_category": "string",
  "images": "array of objects"
}
```

**Content examples**

```json
{
  "id": 167,
  "url": "http://dev.babylandworld.com/apps/product/dell-inspiron-74722670/",
  "active": false,
  "slug": "dell-inspiron-74722670",
  "sku": "null",
  "name": "Dell Inspiron 7472",
  "short_description": "DEll",
  "description": "Dell",
  "creation_date": "2020-08-21T12:45:14.172472+02:00",
  "deliverable": false,
  "stock_amount": 11.0,
  "stock_unit": "pc",
  "weight": 0.0,
  "weight_unit": "null",
  "height": 0.0,
  "height_unit": "null",
  "length": 0.0,
  "length_unit": "null",
  "width": 0.0,
  "width_unit": "null",
  "tax_type": "http://dev.babylandworld.com/apps/tax/43/",
  "manufacturer": "Dell",
  "active_sku": false,
  "active_short_description": false,
  "active_dimension": false,
  "active_weight": false,
  "specification": {
    "specification": {
      "model": "2020best",
      "version": "1"
    },
    "userSpecification": []
  },
  "primary_category": "http://dev.babylandworld.com/apps/category/vehicals/",
  "images": [
    {
      "id": 131,
      "product": 167,
      "name": "04-1-e1517910598586.jpg",
      "image_file": "http://dev.babylandworld.com/media/products/04-1-e1517910598586.jpg"
    }
  ],
  "price": 100000.0,
  "initial_cost": 165000,
  "has_discount": false,
  "discount_percent": 0.0,
  "final_cost": 165000,
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
