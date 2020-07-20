# Create Category

**URL** : `/apps/category/`

**Method** : `POST`

**Auth required** : YES

## Success Response

**Code** : `201 Created`

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
| name `(required)` | string | category name |
| level `(required)` | integer | category level |
