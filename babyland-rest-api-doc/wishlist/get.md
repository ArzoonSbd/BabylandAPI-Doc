[Back](../README.md)

# Get Wishlist

Get Wishlist list if login with valid customer credential.

**URL** : `/apps/wishlist/`

**Method** : `GET`

**Auth required** : Yes

## Success Response

**Code** : `200 OK`

**Response**

```json
{
  "products": [
    {
      "id": 165,
      "url": "http://dev.babylandworld.com/apps/product/remote-car/",
      "relative_url": "vehicals/car/remote-car/",
      "relative_name": [
        {
          "name": "Vehicals",
          "relative_url": "vehicals/"
        },
        {
          "name": "Car",
          "relative_url": "vehicals/car/"
        }
      ],
      "active": true,
      "slug": "remote-car",
      "sku": "20",
      "name": "Remote Car",
      "short_description": "best remote car",
      "description": "spec:\r\n1.\r\n2.\r\n3.",
      "creation_date": "2020-08-19T13:55:11.922460+02:00",
      "deliverable": false,
      "delivery_class": 2,
      "stock_amount": 6.0,
      "stock_unit": "pc",
      "weight": 500.0,
      "weight_unit": "g",
      "height": 0.0,
      "height_unit": "null",
      "length": 0.0,
      "length_unit": "null",
      "width": 0.0,
      "width_unit": "null",
      "tax_type": "http://dev.babylandworld.com/apps/tax/50/",
      "manufacturer": "EVERsoft",
      "active_sku": true,
      "active_short_description": false,
      "active_dimension": true,
      "active_weight": false,
      "specification": {
        "specification": {
          "model": "2020best",
          "version": "1"
        },
        "userSpecification": [
          {
            "id": 1,
            "name": "Color",
            "value": "Red"
          },
          {
            "id": 2,
            "name": "Wifi Enable",
            "value": "Yes"
          }
        ]
      },
      "primary_category": "http://dev.babylandworld.com/apps/category/car/",
      "images": [
        {
          "id": 128,
          "product": 165,
          "name": "home-slider-kidtoys-babylandmall-1.jpg",
          "image_file": "http://dev.babylandworld.com/media/products/home-slider-kidtoys-babylandmall-1.jpg"
        },
        {
          "id": 143,
          "product": 165,
          "name": "Screenshot (1).png",
          "image_file": "http://dev.babylandworld.com/media/products/Screenshot_1_CBUZRpl.png"
        }
      ],
      "price": 1000.0,
      "initial_cost": 1000,
      "has_discount": true,
      "discount_percent": 10.0,
      "final_cost": 900,
      "price_unit": "Nepalese Rupee",
      "fallback_image": "http://dev.babylandworld.com/media/products/defaultImage.png",
      "tags": null
    }
  ]
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
