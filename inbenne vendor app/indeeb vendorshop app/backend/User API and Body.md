

## 1. Register Admin User

Route: /registerAdminUser

Request Body:

- Address1
- Address2
- Pincode
- Number
- PAN
- Password
- Email
- StateName
- UserName

Response:

- 200 OK with admin user object
- 500 Error with error message

## 2. Update Admin User

Route: /updateAdminUser

Request Body:

- UserId
- Address1
- Address2
- Pincode
- Number
- PAN
- Password
- Email
- StateName
- UserName

Response:

- 200 OK with success message
- 500 Error with error message

## 3. Create Vendor Shop

Route: /createVendorShop

Request Body:

- business_name
- gstin
- address_1
- address_2
- pincode
- state_name
- phone_number

Response:

- 201 Created with vendorShopId
- 500 Error with error message

## 4. Admin Login

Route: /adminlogin

Request Body:

- Email
- Password

Response:

- 200 OK with accessToken and refreshToken
- 400 Error with error message

## 5. Register Vendor Shop Employee

Route: /registerVendorShopEmployee

Request Body:

- vendorshop_id
- role
- Address1
- Address2
- pincode
- phone_no
- pan
- password
- email
- state_name
- user_name

Response:

- 200 OK with success message and vendorShopRoleId
- 500 Error with error message

## 6. Login Vendor Shop Employee

Route: /loginVendorShopEmployee

Request Body:

- email
- password

Response:

- 200 OK with accessToken and refreshToken
- 400 Error with error message

## 7. Update Vendor Shop Employee

Route: /updateVendorShopEmployee/:id

Request Body:

- email
- user_name
- pan
- phone_no
- password
- roles_type_id
- state_name
- address_1
- address_2
- pincode
- vendorshop_id

Response:

- 200 OK with success message
- 500 Error with error message

## 8. Get User Info

Route: /getUserInfo/:id

Response:

- 200 OK with user information object
- 404 Not Found if user doesn't exist
- 500 Error with error message

## 9. Get All Users With Vendor Shop Role

Route: /getAllUsersWithVendorShopRole

Response:

- 200 OK with array of user objects
- 500 Error with error message

## 10. Get All Vendor Shops

Route: /getAllVendorShops

Response:

- 200 OK with array of vendor shop objects
- 500 Error with error message

## 11. Register Customer

Route: /registerCustomer

Request Body:

- customer_name
- pan
- phone_no
- gstin
- shop_name
- address_1
- address_2
- pincode
- state_name

Response:

- 200 OK with customerId and customerShopId
- 500 Error with error message

## 12. Get Customer Shops By Vendor Shop Role ID

Route: /getCustomerShopsByVendorShopRoleId

Response:

- 200 OK with array of customer shop objects
- 500 Error with error message