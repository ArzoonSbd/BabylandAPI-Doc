[Back](../README.md)

# Get Product List

Get list of all product.

**URL** : `/apps/product/`

**Method** : `GET`

**Auth required** : NO

## Success Response

**Code** : `200 OK`

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

[Back](../README.md)
