# Django REST API Documentation

running on 'http://dev.babylandworld.com/'.

## Open Endpoints

Open endpoints require no Authentication.

- [Login](login.md) : `POST /api/login/`

## Endpoints that require Authentication

Closed endpoints require a valid Token to be included in the header of the
request. A Token can be acquired from the Login view above.

### Current User related

Each endpoint manipulates or displays information related to the User whose
Token is provided with the request:

- [Get Current User Details](babyland-rest-api-doc/user/get.md) : `GET /api/user/`
- [Get User Details By ID](babyland-rest-api-doc/user/get-id.md) : `GET /api/user/{id}/`
- [Get All User Details](babyland-rest-api-doc/user/get-all.md) : `GET /api/user/all/`
- [Update info](user/put.md) : `PUT /api/user/`
