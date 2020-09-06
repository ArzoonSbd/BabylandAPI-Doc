[Back](../README.md)

# Get collection details

Get details of collection by slug.

**URL** : `/apps/collection/{slug}/`

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

**Reason** : `If invalid or unavailable slug get`

**Response** :

```json
{
  "detail": "Not found."
}
```

[Back](../README.md)
