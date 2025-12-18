# OpenAPI\Client\Axro\AddressApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**billingGetApiV1AddressBillingGet()**](AddressApi.md#billingGetApiV1AddressBillingGet) | **GET** /api/v1/address/billing/ | Get billing address |
| [**shippingCreateApiV1AddressShippingPost()**](AddressApi.md#shippingCreateApiV1AddressShippingPost) | **POST** /api/v1/address/shipping/ | Create shipping address |
| [**shippingGetApiV1AddressShippingGet()**](AddressApi.md#shippingGetApiV1AddressShippingGet) | **GET** /api/v1/address/shipping/ | Get shipping addresses |
| [**shippingGetByIdApiV1AddressShippingShippingAddressIdGet()**](AddressApi.md#shippingGetByIdApiV1AddressShippingShippingAddressIdGet) | **GET** /api/v1/address/shipping/{shipping_address_id} | Get shipping address by ID |
| [**shippingUpdateApiV1AddressShippingShippingAddressIdPut()**](AddressApi.md#shippingUpdateApiV1AddressShippingShippingAddressIdPut) | **PUT** /api/v1/address/shipping/{shipping_address_id} | Update shipping address |


## `billingGetApiV1AddressBillingGet()`

```php
billingGetApiV1AddressBillingGet(): \OpenAPI\Client\Axro\Model\AppSchemasAddressBillingAddressInfo
```

Get billing address

Get the billing address for the current user

### Example

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

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Axro\Model\AppSchemasAddressBillingAddressInfo**](../Model/AppSchemasAddressBillingAddressInfo.md)

### Authorization

[LoginManager](../../README.md#LoginManager)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `shippingCreateApiV1AddressShippingPost()`

```php
shippingCreateApiV1AddressShippingPost($shippingAddressCreate, $check): \OpenAPI\Client\Axro\Model\ResponseShippingCreateApiV1AddressShippingPost
```

Create shipping address

Create a new shipping address. If query parameter check=true is provided, the address is validated and a normalized suggestion is returned without saving.

### Example

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
$shippingAddressCreate = new \OpenAPI\Client\Axro\Model\ShippingAddressCreate(); // \OpenAPI\Client\Axro\Model\ShippingAddressCreate
$check = false; // bool | If true, only checks/normalizes the address via Nominatim and does not save.

try {
    $result = $apiInstance->shippingCreateApiV1AddressShippingPost($shippingAddressCreate, $check);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressApi->shippingCreateApiV1AddressShippingPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **shippingAddressCreate** | [**\OpenAPI\Client\Axro\Model\ShippingAddressCreate**](../Model/ShippingAddressCreate.md)|  | |
| **check** | **bool**| If true, only checks/normalizes the address via Nominatim and does not save. | [optional] [default to false] |

### Return type

[**\OpenAPI\Client\Axro\Model\ResponseShippingCreateApiV1AddressShippingPost**](../Model/ResponseShippingCreateApiV1AddressShippingPost.md)

### Authorization

[LoginManager](../../README.md#LoginManager)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `shippingGetApiV1AddressShippingGet()`

```php
shippingGetApiV1AddressShippingGet(): \OpenAPI\Client\Axro\Model\AppSchemasAddressShippingAddressInfo[]
```

Get shipping addresses

Get all shipping addresses for the current user

### Example

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
    $result = $apiInstance->shippingGetApiV1AddressShippingGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressApi->shippingGetApiV1AddressShippingGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Axro\Model\AppSchemasAddressShippingAddressInfo[]**](../Model/AppSchemasAddressShippingAddressInfo.md)

### Authorization

[LoginManager](../../README.md#LoginManager)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `shippingGetByIdApiV1AddressShippingShippingAddressIdGet()`

```php
shippingGetByIdApiV1AddressShippingShippingAddressIdGet($shippingAddressId): \OpenAPI\Client\Axro\Model\AppSchemasAddressShippingAddressInfo
```

Get shipping address by ID

Return a single shipping address by UUID for the current user.

### Example

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
$shippingAddressId = 'shippingAddressId_example'; // string

try {
    $result = $apiInstance->shippingGetByIdApiV1AddressShippingShippingAddressIdGet($shippingAddressId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressApi->shippingGetByIdApiV1AddressShippingShippingAddressIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **shippingAddressId** | **string**|  | |

### Return type

[**\OpenAPI\Client\Axro\Model\AppSchemasAddressShippingAddressInfo**](../Model/AppSchemasAddressShippingAddressInfo.md)

### Authorization

[LoginManager](../../README.md#LoginManager)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `shippingUpdateApiV1AddressShippingShippingAddressIdPut()`

```php
shippingUpdateApiV1AddressShippingShippingAddressIdPut($shippingAddressId, $shippingAddressUpdate): \OpenAPI\Client\Axro\Model\AppSchemasAddressShippingAddressInfo
```

Update shipping address

Update a shipping address by its ID. Admins can update all fields, users can only update phone and email fields.

### Example

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
$shippingAddressId = 'shippingAddressId_example'; // string
$shippingAddressUpdate = new \OpenAPI\Client\Axro\Model\ShippingAddressUpdate(); // \OpenAPI\Client\Axro\Model\ShippingAddressUpdate

try {
    $result = $apiInstance->shippingUpdateApiV1AddressShippingShippingAddressIdPut($shippingAddressId, $shippingAddressUpdate);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AddressApi->shippingUpdateApiV1AddressShippingShippingAddressIdPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **shippingAddressId** | **string**|  | |
| **shippingAddressUpdate** | [**\OpenAPI\Client\Axro\Model\ShippingAddressUpdate**](../Model/ShippingAddressUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Axro\Model\AppSchemasAddressShippingAddressInfo**](../Model/AppSchemasAddressShippingAddressInfo.md)

### Authorization

[LoginManager](../../README.md#LoginManager)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
