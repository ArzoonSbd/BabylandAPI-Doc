# Get Tax List

Get list of all tax.

**URL** : `/apps/tax/`

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

[Back](../README.md)
