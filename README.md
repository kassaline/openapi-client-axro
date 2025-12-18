# OpenAPIClient-php

The AXRO Sales API provides programmatic access to product information, pricing, inventory, orders and addresses | <a href='/documentation/'>Documentation</a>


## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



// Configure OAuth2 access token for authorization: LoginManager
$config = OpenAPI\Client\Axro\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Axro\Api\AddressApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->billingGetApiV1AddressBillingGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressApi->billingGetApiV1AddressBillingGet: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *http://localhost*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AddressApi* | [**billingGetApiV1AddressBillingGet**](docs/Api/AddressApi.md#billinggetapiv1addressbillingget) | **GET** /api/v1/address/billing/ | Get billing address
*AddressApi* | [**shippingCreateApiV1AddressShippingPost**](docs/Api/AddressApi.md#shippingcreateapiv1addressshippingpost) | **POST** /api/v1/address/shipping/ | Create shipping address
*AddressApi* | [**shippingGetApiV1AddressShippingGet**](docs/Api/AddressApi.md#shippinggetapiv1addressshippingget) | **GET** /api/v1/address/shipping/ | Get shipping addresses
*AddressApi* | [**shippingGetByIdApiV1AddressShippingShippingAddressIdGet**](docs/Api/AddressApi.md#shippinggetbyidapiv1addressshippingshippingaddressidget) | **GET** /api/v1/address/shipping/{shipping_address_id} | Get shipping address by ID
*AddressApi* | [**shippingUpdateApiV1AddressShippingShippingAddressIdPut**](docs/Api/AddressApi.md#shippingupdateapiv1addressshippingshippingaddressidput) | **PUT** /api/v1/address/shipping/{shipping_address_id} | Update shipping address
*InformationApi* | [**getOrderDetailsApiV1InformationOrderDetailOrderNumberGet**](docs/Api/InformationApi.md#getorderdetailsapiv1informationorderdetailordernumberget) | **GET** /api/v1/information/order/detail/{order_number}/ | Get order details
*InformationApi* | [**getOrderListApiV1InformationOrderListGet**](docs/Api/InformationApi.md#getorderlistapiv1informationorderlistget) | **GET** /api/v1/information/order/list/ | Get order list
*InformationApi* | [**getShipmentDetailsApiV1InformationShipmentDetailShipmentNumberGet**](docs/Api/InformationApi.md#getshipmentdetailsapiv1informationshipmentdetailshipmentnumberget) | **GET** /api/v1/information/shipment/detail/{shipment_number}/ | Get shipment details
*InformationApi* | [**getShipmentListApiV1InformationShipmentListGet**](docs/Api/InformationApi.md#getshipmentlistapiv1informationshipmentlistget) | **GET** /api/v1/information/shipment/list/ | Get shipment list
*InformationApi* | [**getTrackingHistoryApiV1InformationTrackingHistoryShipmentNumberGet**](docs/Api/InformationApi.md#gettrackinghistoryapiv1informationtrackinghistoryshipmentnumberget) | **GET** /api/v1/information/tracking/history/{shipment_number}/ | Get tracking history
*LoginApi* | [**loginApiV1LoginPost**](docs/Api/LoginApi.md#loginapiv1loginpost) | **POST** /api/v1/login/ | Login with username and password
*OrderApi* | [**createOrderApiV1OrderPost**](docs/Api/OrderApi.md#createorderapiv1orderpost) | **POST** /api/v1/order/ | Create and place order
*ProductApi* | [**getApiV1ProductGet**](docs/Api/ProductApi.md#getapiv1productget) | **GET** /api/v1/product/ | Get products by filter parameters
*ProductApi* | [**getBrandsApiV1ProductBrandsGet**](docs/Api/ProductApi.md#getbrandsapiv1productbrandsget) | **GET** /api/v1/product/brands/ | Get all available brands
*ProductApi* | [**getCategoriesApiV1ProductCategoriesGet**](docs/Api/ProductApi.md#getcategoriesapiv1productcategoriesget) | **GET** /api/v1/product/categories/ | Get all available categories
*UserApi* | [**readUsersMeApiV1UserInfoGet**](docs/Api/UserApi.md#readusersmeapiv1userinfoget) | **GET** /api/v1/user/info/ | Get user information
*WebhookApi* | [**deleteSubscriptionApiV1WebhookSubscriptionDelete**](docs/Api/WebhookApi.md#deletesubscriptionapiv1webhooksubscriptiondelete) | **DELETE** /api/v1/webhook/subscription/ | Delete webhook subscription
*WebhookApi* | [**getSubscriptionApiV1WebhookSubscriptionGet**](docs/Api/WebhookApi.md#getsubscriptionapiv1webhooksubscriptionget) | **GET** /api/v1/webhook/subscription/ | Get current webhook subscription
*WebhookApi* | [**subscribeApiV1WebhookSubscribePost**](docs/Api/WebhookApi.md#subscribeapiv1webhooksubscribepost) | **POST** /api/v1/webhook/subscribe/ | Create or update webhook subscription

## Models

- [Address](docs/Model/Address.md)
- [AppSchemasAddressBillingAddressInfo](docs/Model/AppSchemasAddressBillingAddressInfo.md)
- [AppSchemasAddressShippingAddressInfo](docs/Model/AppSchemasAddressShippingAddressInfo.md)
- [AppSchemasOrderBillingAddressInfo](docs/Model/AppSchemasOrderBillingAddressInfo.md)
- [AppSchemasOrderShippingAddressInfo](docs/Model/AppSchemasOrderShippingAddressInfo.md)
- [BrandsResponse](docs/Model/BrandsResponse.md)
- [CartItem](docs/Model/CartItem.md)
- [CartItemInfo](docs/Model/CartItemInfo.md)
- [CategoryResponse](docs/Model/CategoryResponse.md)
- [CategoryResponseSchema](docs/Model/CategoryResponseSchema.md)
- [CustomerInfo](docs/Model/CustomerInfo.md)
- [HTTPValidationError](docs/Model/HTTPValidationError.md)
- [LoginResponse](docs/Model/LoginResponse.md)
- [Order](docs/Model/Order.md)
- [OrderDetailItem](docs/Model/OrderDetailItem.md)
- [OrderDetailMessage](docs/Model/OrderDetailMessage.md)
- [OrderDetailsResponse](docs/Model/OrderDetailsResponse.md)
- [OrderInfo](docs/Model/OrderInfo.md)
- [OrderItem](docs/Model/OrderItem.md)
- [OrderListResponse](docs/Model/OrderListResponse.md)
- [PriceResponse](docs/Model/PriceResponse.md)
- [ProductResponse](docs/Model/ProductResponse.md)
- [ProductsResponse](docs/Model/ProductsResponse.md)
- [ResponseShippingCreateApiV1AddressShippingPost](docs/Model/ResponseShippingCreateApiV1AddressShippingPost.md)
- [ShipmentDetailItem](docs/Model/ShipmentDetailItem.md)
- [ShipmentDetailMessage](docs/Model/ShipmentDetailMessage.md)
- [ShipmentDetailsResponse](docs/Model/ShipmentDetailsResponse.md)
- [ShipmentItem](docs/Model/ShipmentItem.md)
- [ShipmentListResponse](docs/Model/ShipmentListResponse.md)
- [ShippingAddressCreate](docs/Model/ShippingAddressCreate.md)
- [ShippingAddressSuggestion](docs/Model/ShippingAddressSuggestion.md)
- [ShippingAddressUpdate](docs/Model/ShippingAddressUpdate.md)
- [SubscribeRequest](docs/Model/SubscribeRequest.md)
- [SubscriptionResponse](docs/Model/SubscriptionResponse.md)
- [TitleResponse](docs/Model/TitleResponse.md)
- [TrackingHistoryResponse](docs/Model/TrackingHistoryResponse.md)
- [User](docs/Model/User.md)
- [ValidationError](docs/Model/ValidationError.md)
- [ValidationErrorLocInner](docs/Model/ValidationErrorLocInner.md)

## Authorization

Authentication schemes defined for the API:
### LoginManager

- **Type**: `OAuth`
- **Flow**: `password`
- **Authorization URL**: ``
- **Scopes**: N/A

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.2.0`
    - Generator version: `7.17.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
