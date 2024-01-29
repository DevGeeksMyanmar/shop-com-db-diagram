# Online Shop Management System Database Requirement Notes

### User Table

- **Admin**
  - id
  - name
  - email
  - password
  - phone number

- **Seller**
  - id
  - name
  - email
  - password
  - phone number

- **Customer**
  - id
  - name
  - email
  - password
  - phone number

### Product Table

- id
- name
- price
- count
- rating
- category_id (foreign key referencing Category)
- seller_id (foreign key referencing Seller)

### Image Table

- id
- image (link or binary data)

### Image - Product Table

- id
- product_id (foreign key referencing Product)
- image_id (foreign key referencing Image)

### Category Table

- id
- name

### Cart Table

- id
- count
- price
- product_id (foreign key referencing Product)
- customer_id (foreign key referencing Customer)

### Order Table

- id
- order_code
- price
- count
- status
- seller_id (foreign key referencing Seller)
- product_id (foreign key referencing Product)
- customer_id (foreign key referencing Customer)
- shipping_id (foreign key referencing Shipping Address)

### Record Table

- id
- order_code
- seller_id (foreign key referencing Seller)
- customer_id (foreign key referencing Customer)
- product_id (foreign key referencing Product)
- price
- count

### Shipping Address Table

- id
- no
- Street
- Township
- City
- Region
- Remark
- customer_id (foreign key referencing Customer)
