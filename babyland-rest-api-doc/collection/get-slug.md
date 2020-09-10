[Back](../README.md)

# Get collection details

Get details of collection by slug. All the product detials listest on the collection are get from the slug.

**URL** : `/apps/collection/{slug}/`

**Method** : `GET`

**Auth required** : NO

## Success Response

**Code** : `200 OK`

**Response**

```json
{
  "id": 10,
  "products": [
    {
      "id": 167,
      "url": "http://dev.babylandworld.com/apps/product/dell-inspiron-74722670/",
      "relative_url": "computer/laptop/dell-inspiron-74722670/",
      "relative_name": [
        {
          "name": "Computer",
          "relative_url": "computer/"
        },
        {
          "name": "Laptop",
          "relative_url": "computer/laptop/"
        }
      ],
      "active": true,
      "slug": "dell-inspiron-74722670",
      "sku": "null",
      "name": "Dell Inspiron 7472",
      "short_description": "i7 processor dell laptop",
      "description": "Dell Mobile Connect is available on all new Bluetooth-enabled, Inspiron, Vostro, G-Series, Alienware and Consumer XPS devices with Windows 10. Dell Mobile Connect’s smartphone Companion App must be downloaded from the App Store for your smartphone, and requires Android 6 (or above) or iOS 11 (or above). For iOS, file transfer capabilities are limited to photos and videos.",
      "creation_date": "2020-08-21T12:45:14.172472+02:00",
      "deliverable": false,
      "delivery_class": 0,
      "stock_amount": 50.0,
      "stock_unit": "pc",
      "weight": 0.0,
      "weight_unit": "null",
      "height": 0.0,
      "height_unit": "null",
      "length": 0.0,
      "length_unit": "null",
      "width": 0.0,
      "width_unit": "null",
      "tax_type": "http://dev.babylandworld.com/apps/tax/51/",
      "manufacturer": "Dell",
      "active_sku": false,
      "active_short_description": false,
      "active_dimension": false,
      "active_weight": false,
      "specification": {
        "specification": {
          "Ram ": "8 GB",
          "Processor": "I3"
        },
        "userSpecification": []
      },
      "primary_category": "http://dev.babylandworld.com/apps/category/laptop/",
      "images": [
        {
          "id": 131,
          "product": 167,
          "name": "04-1-e1517910598586.jpg",
          "image_file": "http://dev.babylandworld.com/media/products/04-1-e1517910598586.jpg"
        }
      ],
      "price": 100000.0,
      "initial_cost": 200000,
      "has_discount": false,
      "discount_percent": 0.0,
      "final_cost": 200000,
      "price_unit": "Nepalese Rupee",
      "fallback_image": "http://dev.babylandworld.com/media/products/defaultImage.png",
      "tags": ""
    }
  ],
  "name": "abcdef",
  "slug": "abcdef",
  "image": "http://dev.babylandworld.com/media/collections/defaultImage.png"
}
```

## Error Response

**Code** : `404 Not Found`

**Reason** : `If invalid or unavailable slug get`

**Response** :

```json
{
  "detail": "Not found."
}
```

[Back](../README.md)
