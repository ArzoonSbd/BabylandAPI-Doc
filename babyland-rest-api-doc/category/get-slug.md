[Back](../README.md)

# Get Category By Slug

Get detail of a category with given slug.

**URL** : `/apps/category/{slug}/`

**Method** : `GET`

**Auth required** : NO

## Success Response

**Code** : `200 OK`

**JSON representation**

```json
{
  "id": "integer",
  "url": "string",
  "name": "string",
  "level": "integer",
  "parent": "string",
  "specification": "object",
  "products": "Array of strings"
}
```

**Content examples**

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

## Failure Response

**Code** : `404 Not Found`

**JSON representation**

```json
{
  "detail": "Not found."
}
```

**Reason** : `Category with the given slug doesn't exist.`

[Back](../README.md)
