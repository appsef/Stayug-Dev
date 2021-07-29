# REST API DOC

Stayug's REST API's Doc

``` kotlin
ip : 
port : 
```


Property | Type | Description
------------ | ------------- | -------------
productSKU | VARCHAR(45) | Primary key
productName | TEXT | Title of product
productDescription | TEXT | Product Description
productAttributes | JSON | Highlights of product
productImages | JSON | Array of image links
productMRP | DOUBLE | Market Price
categoryTags | JSON | Array of tags
productBrand | VARCHAR(45) | Product Brand
productInStock | TINYINT(1) | 0 = Out of, 1 = In Stock
productRate | DECIMAL(3,2) | Product Rate
codAvailable | TINYINT(1) | 0 = No, 1 = Yes
returnAvailable | TINYINT(1) | 0 = No, 1 = Yes

> Get list of products(demo) - testing only

To get list of all products

``` html
GET <ip>:<port>/products/all 
```

To get sorted list of products 

``` html
GET <ip>:<port>/products/tags/:tag 
GET <ip>:<port>/products/tags/:tag?sort=LTH/HTL/RATE
```

 this will return a sorted list of products
 > `:tag` is category tag like SCHOOL, NOTEBOOK, PEN etc.
 >  * LTH = Low To High (Price)
 >  * HTL = High To Low (Price)
 >  * RATE = Top Rated (Product Rating)


To get a single product by productSKU

``` html
GET <ip>:<port>/products/sku/:productSKU
```


#### Tasks

- [x] Products List
- [ ] WishList Operations
- [ ] Order Operations
- [ ] Cart Operations
