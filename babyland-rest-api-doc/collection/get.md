[Back](../README.md)

# Get collection List

Get details of collection.

**URL** : `/apps/collection/`

**Method** : `GET`

**Auth required** : NO

## Success Response

**Code** : `200 OK`

**Response**

```json
{
  "id": 1,
  "products": [178],
  "name": "car",
  "slug": "car",
  "image": "http://dev.babylandworld.com/media/collections/defaultImage.png"
}
```

## Error Response

**Code** : `404 Not Found`

**Reason** : `If call invalid URL`

**Response** :

```json
{
  "detail": "Page not found at /apps/collectio/"
}
```

[Back](../README.md)
