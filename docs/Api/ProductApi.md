# OpenAPI\Client\Axro\ProductApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getApiV1ProductGet()**](ProductApi.md#getApiV1ProductGet) | **GET** /api/v1/product/ | Get products by filter parameters |
| [**getBrandsApiV1ProductBrandsGet()**](ProductApi.md#getBrandsApiV1ProductBrandsGet) | **GET** /api/v1/product/brands/ | Get all available brands |
| [**getCategoriesApiV1ProductCategoriesGet()**](ProductApi.md#getCategoriesApiV1ProductCategoriesGet) | **GET** /api/v1/product/categories/ | Get all available categories |


## `getApiV1ProductGet()`

```php
getApiV1ProductGet($format, $productNumber, $oem, $ean, $brand, $category, $page, $limit): \OpenAPI\Client\Axro\Model\ProductsResponse
```

Get products by filter parameters

Get products by filter parameters

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: LoginManager
$config = OpenAPI\Client\Axro\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Axro\Api\ProductApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$format = 'format_example'; // string | Possible values: json or xml (BMEcat 2005 format)
$productNumber = ; // string | Use single or comma-separated AXRO numbers (Product Numbers)
$oem = ; // string | Use single or comma-separated OEM numbers
$ean = ; // string | Use single or comma-separated EAN numbers
$brand = ; // string | Use single or comma seperated brand names (can combined with category)
$category = ; // string | Use single or comma seperated category ids. Fetch via categories endpoint. (can combined with brand)
$page = 1; // int
$limit = 100; // int

try {
    $result = $apiInstance->getApiV1ProductGet($format, $productNumber, $oem, $ean, $brand, $category, $page, $limit);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->getApiV1ProductGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **format** | **string**| Possible values: json or xml (BMEcat 2005 format) | [optional] |
| **productNumber** | **string**| Use single or comma-separated AXRO numbers (Product Numbers) | [optional] |
| **oem** | **string**| Use single or comma-separated OEM numbers | [optional] |
| **ean** | **string**| Use single or comma-separated EAN numbers | [optional] |
| **brand** | **string**| Use single or comma seperated brand names (can combined with category) | [optional] |
| **category** | **string**| Use single or comma seperated category ids. Fetch via categories endpoint. (can combined with brand) | [optional] |
| **page** | **int**|  | [optional] [default to 1] |
| **limit** | **int**|  | [optional] [default to 100] |

### Return type

[**\OpenAPI\Client\Axro\Model\ProductsResponse**](../Model/ProductsResponse.md)

### Authorization

[LoginManager](../../README.md#LoginManager)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`, `application/xml`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBrandsApiV1ProductBrandsGet()`

```php
getBrandsApiV1ProductBrandsGet(): \OpenAPI\Client\Axro\Model\BrandsResponse
```

Get all available brands

Get all available brands

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: LoginManager
$config = OpenAPI\Client\Axro\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Axro\Api\ProductApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getBrandsApiV1ProductBrandsGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->getBrandsApiV1ProductBrandsGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Axro\Model\BrandsResponse**](../Model/BrandsResponse.md)

### Authorization

[LoginManager](../../README.md#LoginManager)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCategoriesApiV1ProductCategoriesGet()`

```php
getCategoriesApiV1ProductCategoriesGet(): \OpenAPI\Client\Axro\Model\CategoryResponseSchema[]
```

Get all available categories

Get all available categories

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: LoginManager
$config = OpenAPI\Client\Axro\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Axro\Api\ProductApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getCategoriesApiV1ProductCategoriesGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductApi->getCategoriesApiV1ProductCategoriesGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Axro\Model\CategoryResponseSchema[]**](../Model/CategoryResponseSchema.md)

### Authorization

[LoginManager](../../README.md#LoginManager)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
