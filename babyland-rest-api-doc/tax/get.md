# Get Tax List

**URL** : `/apps/tax/`

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
  "percent": "number"
}
```

**Content examples**

```json
{
  "id": 37,
  "url": "http://dev.babylandworld.com/apps/tax/37/",
  "name": "zero tax",
  "percent": 0.0
}
```

**Parameters**
| Field | Type | Description |
| :---------- | :----: | ---------------: |
| id | integer | tax id |
| url | string | tax url|
| name | string | tax name |
| percent | number | tax percent |
