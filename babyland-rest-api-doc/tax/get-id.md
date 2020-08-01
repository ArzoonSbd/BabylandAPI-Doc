[Back](../README.md)

# Get Tax By ID

Get detail of a tax with given id.

**URL** : `/apps/tax/{id}/`

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

## Failure Response

**Code** : `404 Not Found`

**JSON representation**

```json
{
  "detail": "Not found."
}
```

**Reason** : `Tax with the given id doesn't exist.`

[Back](../README.md)
