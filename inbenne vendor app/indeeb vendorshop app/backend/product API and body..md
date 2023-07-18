
# API Documentation

## Brand APIs
### Create Brand

POST /brands

Creates a new brand and links it to the vendor shop role of the authenticated user.

Request Body:

{
  "brand_name": "String"
}

Response (201):  

{
  "message": "Brand created successfully",
  "brandId": "Number"   
}

### Get Brand By ID

GET /brands/:id

Gets a brand by ID that is linked to the vendor shop role of the authenticated user.

Response (200):

{
  "id": "Number",
  "brand_name": "String",
  "added_by": "Number"
}

### Get All Brands  

GET /brands

Gets all brands linked to the vendor shop role of the authenticated user.

Response (200):  

[
  {
    "id": "Number",
    "brand_name": "String",
    "added_by": "Number"
  },
  ...
]

## Unit APIs  

### Create Unit   

POST /units

Creates a new unit and links it to the vendor shop role of the authenticated user.

Request Body:

{
  "unit_name": "String"   
}

Response (201):

{
  "message": "Unit created successfully",
  "unitId": "Number"  
}

### Get Units   

GET /units

Gets all units linked to the vendor shop role of the authenticated user.

Response (200):

[
  {
    "id": "Number", 
    "unit_name": "String",
    "added_by": "Number"
  },
  ...
]

### Get Unit By ID  

GET /units/:id

Gets a unit by ID that is linked to the vendor shop role of the authenticated user.

Response (200):  

{
  "id": "Number",
  "unit_name": "String",
  "added_by": "Number"   
}

### Update Unit  

PUT /units/:id

Updates a unit by ID that is linked to the vendor shop role of the authenticated user.  

Request Body:

{
  "unit_name": "String"    
}

Response (200): 

{
  "message": "Unit updated successfully",
  "unitId": "Number" 
}

## HSN APIs   

### Create HSN

POST /hsn

Creates a new HSN code and links it to the vendor shop role of the authenticated user.

Request Body:  

{
  "code": "String",
  "gst_rate": "Number",
  "cgst_rate": "Number",
  "sgst_rate": "Number",
  "igst_rate": "Number"   
}

Response (201):  

{
  "message": "HSN created successfully",
  "hsnId": "Number"  
}

### Get HSN By ID  

GET /hsn/:id

Gets an HSN by ID that is linked to the vendor shop role of the authenticated user.   

Response (200):

{
  "id": "Number",
  "code": "String",
  "gst_rate": "Number",
  "cgst_rate": "Number",
  "sgst_rate": "Number",
  "igst_rate": "Number",
  "added_by": "Number"    
}

### Get All HSNs

GET /hsn  

Gets all HSN codes linked to the vendor shop role of the authenticated user.

Response (200):   

[
  {
    "id": "Number",
    "code": "String",
    "gst_rate": "Number",
    "cgst_rate": "Number",
    "sgst_rate": "Number",
    "igst_rate": "Number",
    "added_by": "Number"
  },
  ...
]

### Update HSN   

PUT /hsn/:id

Updates an HSN by ID that is linked to the vendor shop role of the authenticated user.

Request Body:   

{
  "code": "String",
  "gst_rate": "Number",
  "cgst_rate": "Number", 
  "sgst_rate": "Number",
  "igst_rate": "Number"   
}

Response (200):  

{
  "message": "HSN updated successfully",
  "hsnId": "Number"   
}

## Product APIs    

### Create Product   

POST /products  

Creates a new product and links it to the vendor shop role of the authenticated user.     

Request Body:  

{
  "product_name": "String",
  "brand_id": "Number",
  "hsn_id": "Number"    
}

Response (201):  

{
  "message": "Product created successfully",
  "productId": "Number"    
}

### Get Products  

GET /products  

Gets all products linked to the vendor shop role of the authenticated user.

Response (200):   

[
  {
    "id": "Number",  
    "product_name": "String", 
    "brand_id": "Number",
    "hsn_id": "Number",
    "added_by": "Number"
  },
  ...  
]

### Get Product By ID   

GET /products/:id  

Gets a product by ID that is linked to the vendor shop role of the authenticated user. 

Response (200):

{
  "id": "Number", 
  "product_name": "String",
  "brand_id": "Number",
  "hsn_id": "Number",
  "added_by": "Number"   
}

### Update Product  

PUT /products/:id

Updates a product by ID that is linked to the vendor shop role of the authenticated user.     

Request Body:

{
  "product_name": "String",
  "brand_id": "Number",
  "hsn_id": "Number"     
}

Response (200):  

{
  "message": "Product updated successfully",
  "productId": "Number"  
}

### Delete Product   

DELETE /products/:id  

Deletes a product by ID that is linked to the vendor shop role of the authenticated user.

Response (200):    

{
  "message": "Product deleted successfully",
  "productId": "Number"   
}

## Variant APIs  

### Create Variant  

POST /variants   

Creates a new product variant and links it to the vendor shop role of the authenticated user.

Request Body:  

{
  "product_id": "Number",
  "unit_id": "Number",
  "variant_name": "String",
  "price": "Number",
  "quantity": "Number",
  "order_quantity": "Number", 
  "mrp": "Number"  
}

Response (201):   

{
  "message": "Variant created successfully",
  "variantId": "Number"    
}

### Get Variants

GET /variants  

Gets all variants linked to the vendor shop role of the authenticated user.

Response (200):  

[
  {
    "id": "Number",
    "product_id": "Number",
    "unit_id": "Number",  
    "variant_name": "String",
    "price": "Number",
    "quantity": "Number",
    "order_quantity": "Number",
    "mrp": "Number",
    "added_by": "Number"
  },
  ...
]

### Get Variant By ID   

GET /variants/:id

Gets a variant by ID that is linked to the vendor shop role of the authenticated user.

Response (200):  

{
  "id": "Number",
  "product_id": "Number",
  "unit_id": "Number",
  "variant_name": "String",
  "price": "Number",
  "quantity": "Number",
  "order_quantity": "Number",
  "mrp": "Number",
  "added_by": "Number"  
}

### Update Variant    

PUT /variants/:id  

Updates a variant by ID that is linked to the vendor shop role of the authenticated user.  

Request Body:

{
  "product_id": "Number",
  "unit_id": "Number", 
  "variant_name": "String",
  "price": "Number",
  "quantity": "Number",
  "order_quantity": "Number",
  "mrp": "Number"   
}

Response (200):  

{
  "message": "Variant updated successfully",
  "variantId": "Number"   
}

### Delete Variant  

DELETE /variants/:id

Deletes a variant by ID that is linked to the vendor shop role of the authenticated user. 

Response (200):     

{
  "message": "Variant deleted successfully",
  "variantId": "Number"  
}

## Order APIs  

### Create Order     

POST /orders  

Creates a new order for the given customer and links it to the vendor shop of the authenticated user.  

Request Body:     

{
  "customer_id": "Number",
  "order_items": [
    {
      "product_name": "String",
      "variant_price": "Number",  
      "gst_price": "Number",
      "selling_price": "Number",
      "max_retail_price": "Number",
      "quantity": "Number"
    },
    ...
  ]
}

Response (201):  

{
  "message": "Order created successfully",
  "orderId": "Number",
  "transactionId": "Number"   
}

### Get Order By ID  

GET /orders/:id  

Gets an order by ID, along with order items and customer name. Accessible only if the order belongs to the authenticated user's vendor shop or customer.

Response (200):

{
  "order": {
    "id": "Number",
    "order_status": "String",
    "added_by": "Number",
    "customer_shops": "Number"
  },
  "customer_name": "String",
  "items": [
    {
      "id": "Number",
      "order_id": "Number",
      "product_name": "String",
      ...
    },
    ...
  ]
}

### Delete Order     

DELETE /orders/:id   

Deletes an order by ID. Only possible if the order belongs to the authenticated user's vendor shop.  

Response (200):  

{
  "message": "Order deleted successfully"  
}

## Price Allowance APIs     

### Create Allowance  

POST /allowance  

Creates a new price allowance percentage for the vendor shop of the authenticated user.

Request Body:  

{
  "allowance": "Number"    
}

Response (201):

{
  "message": "Price allowance created successfully",
  "allowanceId": "Number"  
}

### Update Allowance   

PUT /allowance/:id 

Updates the price allowance percentage for the vendor shop of the authenticated user.     

Request Body:

{
  "allowance": "Number"     
}

Response (200):

{
  "message": "Price allowance updated successfully"  
}

### Get Allowance

GET /allowance/:id

Gets the price allowance for the vendor shop of the authenticated user.

Response (200): 

{
  "id": "Number",
  "allowance": "Number", 
  "added_by": "Number"
}

### Delete Allowance  

DELETE /allowance/:id  

Deletes the price allowance for the vendor shop of the authenticated user.

Response (200): 

{
  "message": "Price allowance deleted successfully"
}