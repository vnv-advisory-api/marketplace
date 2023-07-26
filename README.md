# VNVAdvisory Marketplace Data - Demo Endpoint

## Overview

The WooCommerce API with Extended Functionality allows developers to interact with WooCommerce stores and access specific products with enhanced security using the `x-api-key` header. As part of the test environment, you can use the demo endpoint to retrieve sample data for product ID 766.

## Demo Endpoint

The demo endpoint URL for retrieving product data is:

```
https://market.vnvadvisory.com/wp-json/wc/v3/products/766
```

### Required Headers

To access the demo data, make sure to include the following headers in your GET request:

- **x-api-key**: iSGEdDpy4WLvj3Qm7pCogy6V

Example using cURL:

```bash
curl -X GET "https://market.vnvadvisory.com/wp-json/wc/v3/products/766" \
  -H "x-api-key: test_x-api-key"
```

### Query Parameters

In addition to the headers, please include the following query parameters for authentication:

- **consumer_key**: ck_93033ba6977158a41fbb48ce879704789931da49
- **consumer_secret**: cs_f0eea610ba99e29e3b0164c9c03d5cb33574905a

Example using cURL:

```bash
curl -X GET "https://market.vnvadvisory.com/wp-json/wc/v3/products/766?consumer_key=test_consumer_key&consumer_secret=test_consumer_secret" \
  -H "x-api-key: test_x-api-key"
```

### Response

The API will respond with a JSON object containing the demo data for the product with ID 766:
```json
{
  "id": 766,
  "name": "Demo Product",
  "price": "19.99",
  "description": "This is a demo product for testing purposes.",
  "category": "Demo Category",
  "stock_quantity": 100,
  "image": "https://example.com/demo_product.jpg"
  // Additional product details...
}
```

Please note that this is sample data and does not reflect actual product information.

## Get Started
If you want access to real VNV products and data please click [HERE](https://market.vnvadvisory.com/request-info/)  to fill the form and we'll get back to you.

## Contribution

Contributions to the WooCommerce API with Extended Functionality are welcome! If you encounter any bugs, have feature requests, or want to improve the documentation, please submit an issue or a pull request to this repository.

