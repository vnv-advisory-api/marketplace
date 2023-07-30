# VNVAdvisory Marketplace Data - Demo Endpoint

## Overview

The **WooCommerce API with Extended Functionality** enables developers to interact with WooCommerce stores and access specific products with enhanced security using the `x-api-key` header. In this test environment, you can utilize the demo endpoint to retrieve sample data for a particular product (ID 829).

## Aim and Purpose
The aim of this code is to provide developers with an automated way to access live volumes of certified carbon credits from project developer [VNV Advisory based in Bangalore, India](https://www.vnvadvisory.com). VNV Advisory is a project developer with over 15 years of experience committed to environmental sustainability and social impact. We are not just another commodity trader or fancy retailer with beautiful stories; instead, we take pride in being the real deal. Our approach revolves around brokering credits on behalf of the 150 (!) certified projects we develop in collaboration with our dedicated social partners on the ground.

Through our platform and API, we enable developers to seamlessly participate in carbon credit transactions, promoting sustainable practices and making a meaningful impact on the planet.

1. **Request Private Keys:**
   To get started, you'll need private keys that can be requested [here](https://market.vnvadvisory.com/request-info/). These private keys are crucial for authentication and secure access to the marketplace.

2. **Connect Keys to Specific Volumes:**
   We understand the importance of granularity and control. Our extended functionality allows us to connect specific API keys to specific products (volumes) rather than granting all keys access to all products. We'll assist you in linking your keys to the volume(s) from which you would like to reserve credits (i.e. biogas, cookstoves, clean water, wind, solar etc).

3. **Purchase Certified Carbon Credits:**
   With the obtained private keys, developers can buy certified carbon credits with volumes as low as 10 credits (equivalent to 10 tonnes of certified CO2 compensation). Upon making the purchase, you will be presented with an online payment option. In case your specific business requires another approach (say weekly or monthly retirements), we can work out the best process together.

4. **Customized Credit Retirement:**
   During the purchasing process, you can provide a description that you want VNV to use when retiring these credits on your behalf. Typically, we work with the phrase: *"Retired on behalf of <X> to offset their <scope X> emissions for year(s) 2022-2023"* or something along those lines.

After the payment has been successfully transferred, VNV's Portfolio team will process your request. Within 2-5 business days, you will receive the public GoldStandard or VERRA link that verifies the retirement of carbon credits on your behalf.

Please note that the provided data in this demo endpoint is for demonstration purposes only and does not represent actual product information.

## Demo Endpoint

The demo endpoint URL for retrieving product data is:

```
https://market.vnvadvisory.com/wp-json/wc/v3/products/829
```

## Required Headers

To access the demo data, ensure that you include the following headers in your GET request:

```
x-api-key: iSGEdDpy4WLvj3Qm7pCogy6V
```

**Example using cURL:**

```bash
curl -X GET "https://market.vnvadvisory.com/wp-json/wc/v3/products/829" \
  -H "x-api-key: test_x-api-key"
```

## Query Parameters

In addition to the headers, please include the following query parameters for authentication:

```
consumer_key: ck_93033ba6977158a41fbb48ce879704789931da49
consumer_secret: cs_f0eea610ba99e29e3b0164c9c03d5cb33574905a
```

**Example using cURL:**

```bash
curl -X GET "https://market.vnvadvisory.com/wp-json/wc/v3/products/829?consumer_key=test_consumer_key&consumer_secret=test_consumer_secret" \
  -H "x-api-key: test_x-api-key"
```

## Response

The API will respond with a JSON object containing the demo data for the product with ID 829:

```json
{
    "id": 829,
    "name": "GSXX123 (test-product)",
    "slug": "gsxx123-test-product",
    "permalink": "https://market.vnvadvisory.com/product/gsxx123-test-product/",
    "date_created": "2023-07-05T08:38:54",
    "date_created_gmt": "2023-07-05T08:38:54",
    "date_modified": "2023-07-05T08:40:44",
    "date_modified_gmt": "2023-07-05T08:40:44",
    "type": "simple",
    "status": "publish",
    "featured": false,
    "catalog_visibility": "visible",
    // Additional product details...
}
```

Please note that this data is for demonstration purposes only and does not represent actual product information.

## Get Started

If you are interested in accessing real VNV products and data, please click [HERE](https://vnvadvisory.com/real-products-form) to fill out the form, and we'll get back to you promptly.

## Contribution

Contributions to the WooCommerce API with Extended Functionality are most welcome! If you encounter any bugs, have feature requests, or want to improve the documentation, please feel free to submit an issue or a pull request to this repository.
