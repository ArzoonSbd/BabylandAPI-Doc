# Show Current User

Get the details of the currently Authenticated User along with basic
subscription information.

**URL** : `/api/user/`

**Method** : `GET`

**Auth required** : YES

**Permissions required** : None

## Success Response

**Code** : `200 OK`

**Content examples**

For a User with ID 45 on the local database where that User has saved an
email address and name information.

```json
{
  "id": 45,
  "first_name": "arjun",
  "last_name": "subedi",
  "date_joined": "2020-07-12T17:32:33.831257+02:00",
  "is_active": true,
  "email": "arjun.eversoft@gmail.com",
  "gender": "M",
  "phone": "9806633448",
  "avatar": "/media/admin/defaultAvatar.png",
  "role": 0,
  "last_login": "2020-07-13T18:43:55.024820+02:00"
}
```

For a user with ID 45 on the local database but no details have been set yet.

```json
{
  "id": 45,
  "first_name": "",
  "last_name": "",
  "date_joined": "",
  "is_active": true,
  "email": "",
  "gender": "",
  "phone": "",
  "avatar": "/media/admin/defaultAvatar.png",
  "role": 0,
  "last_login": "2020-07-13T18:43:55.024820+02:00"
}
```

## Notes

- If the User does not have a `UserInfo` instance when requested then one will
  be created for them.
