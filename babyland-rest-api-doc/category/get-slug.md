[Back](../README.md)

# Get Category By Slug

Get detail of a category with given slug.

**URL** : `/apps/category/{slug}/`

**Method** : `GET`

**Auth required** : Yes

## Success Response

**Code** : `200 OK`

**Response**

```json
{
  "id": 192,
  "url": "http://dev.babylandworld.com/apps/category/computer/",
  "name": "Computer",
  "level": 0,
  "parent": null,
  "specification": [
    {
      "id": 0,
      "name": "Ram ",
      "type": "selection",
      "default": "4 GB",
      "options": ["8 GB", "4 GB"]
    },
    {
      "id": 1,
      "name": "Processor",
      "type": "selection",
      "default": "I3",
      "options": ["I5", "I3", "I7"]
    }
  ],
  "children": [193, 194],
  "slug": "computer",
  "image": "http://dev.babylandworld.com/media/category/images/cover_letter_of.com.np.jpg"
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

**Code** : `404 Not Found`

**JSON representation**

```json
{
  "detail": "Not found."
}
```

**Reason** : `Category with the given slug doesn't exist.`

[Back](../README.md)
