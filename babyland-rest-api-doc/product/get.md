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
        "for_sale": false,
        "for_sale_percent": 0.0,
        "for_sale_price": 0.0,
        "creation_date": "2020-07-18T17:42:53.729223+02:00",
        "deliverable": true,
        "stock_amount": 20.0,
        "stock_unit": "piece",
        "weight": 1.0,
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
    },
```

[Back](../README.md)
