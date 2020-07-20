# Get Category List

**URL** : `/apps/category/`

**Method** : `GET`

**Auth required** : YES

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
  "id": 118,
  "url": "http://dev.babylandworld.com/apps/category/118/",
  "name": "Dell Laptop",
  "level": 1,
  "parent": "http://dev.babylandworld.com/apps/category/117/",
  "specification": [
    {
      "id": 0,
      "name": "Ram",
      "type": "selection",
      "default": "",
      "options": ["2gb"]
    },
    {
      "id": 1,
      "name": "Core Processor",
      "type": "text",
      "default": "i3"
    },
    {
      "id": 2,
      "name": "Keyboard",
      "type": "number",
      "default": "2pcs"
    }
  ],
  "products": ["http://dev.babylandworld.com/apps/product/109/"]
}
```

**Parameters**
| Field | Type | Description |
| :---------- | :----: | ---------------: |
| id | integer | category id |
| url | string | category url|
| name | string | category name |
| level | integer | category level |
| parent | string | parent category |
| specification | object | category specification |
| products | array of strings | products |
