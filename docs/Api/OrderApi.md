# OpenAPI\Client\Axro\OrderApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createOrderApiV1OrderPost()**](OrderApi.md#createOrderApiV1OrderPost) | **POST** /api/v1/order/ | Create and place order |


## `createOrderApiV1OrderPost()`

```php
createOrderApiV1OrderPost($order, $place): \OpenAPI\Client\Axro\Model\OrderInfo
```

Create and place order

Create an order with the given cart items. To place the order, add the query parameter 'place'.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: LoginManager
$config = OpenAPI\Client\Axro\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Axro\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order = new \OpenAPI\Client\Axro\Model\Order(); // \OpenAPI\Client\Axro\Model\Order
$place = false; // bool | Set to true to place the order

try {
    $result = $apiInstance->createOrderApiV1OrderPost($order, $place);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->createOrderApiV1OrderPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order** | [**\OpenAPI\Client\Axro\Model\Order**](../Model/Order.md)|  | |
| **place** | **bool**| Set to true to place the order | [optional] [default to false] |

### Return type

[**\OpenAPI\Client\Axro\Model\OrderInfo**](../Model/OrderInfo.md)

### Authorization

[LoginManager](../../README.md#LoginManager)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
