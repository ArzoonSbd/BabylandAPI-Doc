### Authorization API

Autorization API Endpoints listed below:

- [Staff/Admin login](authorization/admin.md) : `POST /api/token/obtain/`
- [Customer login](authorization/customer.md) : `POST /api/customer/token/obtain/`
- [Token Blacklist](authorization/token-blacklist.md) : `POST /api/token/blacklist/`
- [Refresh Token](authorization/refresh-token.md) : `POST /api/token/refresh/`
- [Token Validation](authorization/token-validation.md) : `POST /api/token/valid/`
- [Email Activation](authorization/account-activate.md) : `POST /api/user/activate/`
- [Forget Password](authorization/forget-password.md) : `POST /api/user/forget/`
- [Reset Password](authorization/reset-password.md) : `POST /api/user/reset/`
- [Change Password](authorization/change-password.md) : `PUT /api/user/password/`

### Category API

Category API Endpoints listed below:

- [Get all Category](category/get.md) : `GET /apps/category/`
- [Get Category details by Slug](category/get-slug.md) : `GET /apps/category/{slug}/`
- [Create Category](category/post.md) : `POST /apps/category/`
- [Update Category by Slug](category/put.md) : `PUT /apps/category/{slug}/`
- [Partial Update Category by Slug](category/patch.md) : `PATCH /apps/category/{slug}/`

- [Delete Category by Slug](category/delete.md) : `DELETE /apps/category/{slug}/`

### Customer API

Customer API Endpoints listed below:

- [Get all Customer detials](customer/get-all.md) : `GET /api/customer/all/`
- [Get current Customer](customer/get.md) : `GET /api/customer`
- [Get Customer details by ID](customer/get-id.md) : `GET /api/customer/{id}/`
- [Create Customer](customer/post.md) : `POST /api/customer/`
- [Update Customer by ID](customer/put.md) : `PUT /api/customer/{id}/`
- [Partial Update Customer](customer/patch.md) : `PATCH /api/customer/`
- [Partial Update Customer by ID](customer/patch-id.md) : `PATCH /api/customer/{id}/`

- [Delete Customer by ID](customer/delete.md) : `DELETE /api/customer/{id}/`

### Product API

Product API Endpoints listed below:

- [Get all Products](product/get.md) : `GET /apps/product/`
- [Get Product details by Slug](product/get-slug.md) : `GET /apps/product/{slug}/`
- [Create Product](product/post.md) : `POST /apps/Product/`
- [Update Product by Slug](product/put.md) : `PUT /apps/product/{slug}/`
- [Partial Update Product by Slug](product/patch.md) : `PATCH /apps/product/{slug}/`

- [Delete Product by Slug](product/delete.md) : `DELETE /apps/product/{slug}/`

### Tax API

Tax API Endpoints listed below:

- [Get all Tax](tax/get.md) : `GET /apps/tax/`
- [Get Tax details by ID](tax/get-id.md) : `GET /apps/tax/{id}/`
- [Create Tax](tax/post.md) : `POST /apps/tax/`
- [Update Tax by ID](tax/put.md) : `PUT /apps/tax/{id}/`
- [Partial Update Tax by ID](tax/patch.md) : `PATCH /apps/tax/{id}/`

- [Delete Tax by ID](tax/delete.md) : `DELETE /apps/tax/{id}/`

### User API

User API Endpoints listed below:

- [Get all User details](user/get-all.md) : `GET /api/user/all/`
- [Get current User details](user/get.md) : `GET /api/user/`
- [Get User details by ID](user/get-id.md) : `GET /api/user/{id}/`

- [Create User](user/post.md) : `POST /api/user/`
- [Update User details](user/put-id.md) : `PUT /api/user/{id}/`
- [Partial Update User details](user/patch.md) : `PATCH /api/user/`
- [Partial Update User details by ID](user/patch-id.md) : `PUT /api/user/{id}/`
- [Delete User by ID](user/delete-id.md) : `DELETE /api/user/{id}/`
- [Delete User](user/delete.md) : `DELETE /api/user/`

### Wishlist API

Wishlist API Endpoints listed below:

- [Get Wishlist](wishlist/get.md) : `GET /apps/wishlist/`
- [Create Wishlist](wishlist/post.md) : `POST /apps/wishlist/`

- [Delete Wishlist](wishlist/delete.md) : `DELETE /apps/wishlist/`

### Cart API

Cart API Endpoints listed below:

- [Get Cart](cart/get.md) : `GET /apps/cart/`
- [Create Cart](cart/post.md) : `POST /apps/cart/`
  [Back](../README.md)
