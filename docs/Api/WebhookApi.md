# OpenAPI\Client\Axro\WebhookApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteSubscriptionApiV1WebhookSubscriptionDelete()**](WebhookApi.md#deleteSubscriptionApiV1WebhookSubscriptionDelete) | **DELETE** /api/v1/webhook/subscription/ | Delete webhook subscription |
| [**getSubscriptionApiV1WebhookSubscriptionGet()**](WebhookApi.md#getSubscriptionApiV1WebhookSubscriptionGet) | **GET** /api/v1/webhook/subscription/ | Get current webhook subscription |
| [**subscribeApiV1WebhookSubscribePost()**](WebhookApi.md#subscribeApiV1WebhookSubscribePost) | **POST** /api/v1/webhook/subscribe/ | Create or update webhook subscription |


## `deleteSubscriptionApiV1WebhookSubscriptionDelete()`

```php
deleteSubscriptionApiV1WebhookSubscriptionDelete($customerNumber)
```

Delete webhook subscription

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: LoginManager
$config = OpenAPI\Client\Axro\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Axro\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$customerNumber = 'customerNumber_example'; // string

try {
    $apiInstance->deleteSubscriptionApiV1WebhookSubscriptionDelete($customerNumber);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->deleteSubscriptionApiV1WebhookSubscriptionDelete: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **customerNumber** | **string**|  | [optional] |

### Return type

void (empty response body)

### Authorization

[LoginManager](../../README.md#LoginManager)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSubscriptionApiV1WebhookSubscriptionGet()`

```php
getSubscriptionApiV1WebhookSubscriptionGet($customerNumber): \OpenAPI\Client\Axro\Model\SubscriptionResponse
```

Get current webhook subscription

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: LoginManager
$config = OpenAPI\Client\Axro\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Axro\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$customerNumber = 'customerNumber_example'; // string

try {
    $result = $apiInstance->getSubscriptionApiV1WebhookSubscriptionGet($customerNumber);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->getSubscriptionApiV1WebhookSubscriptionGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **customerNumber** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Axro\Model\SubscriptionResponse**](../Model/SubscriptionResponse.md)

### Authorization

[LoginManager](../../README.md#LoginManager)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `subscribeApiV1WebhookSubscribePost()`

```php
subscribeApiV1WebhookSubscribePost($subscribeRequest, $customerNumber): \OpenAPI\Client\Axro\Model\SubscriptionResponse
```

Create or update webhook subscription

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: LoginManager
$config = OpenAPI\Client\Axro\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Axro\Api\WebhookApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$subscribeRequest = new \OpenAPI\Client\Axro\Model\SubscribeRequest(); // \OpenAPI\Client\Axro\Model\SubscribeRequest
$customerNumber = 'customerNumber_example'; // string

try {
    $result = $apiInstance->subscribeApiV1WebhookSubscribePost($subscribeRequest, $customerNumber);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WebhookApi->subscribeApiV1WebhookSubscribePost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **subscribeRequest** | [**\OpenAPI\Client\Axro\Model\SubscribeRequest**](../Model/SubscribeRequest.md)|  | |
| **customerNumber** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Axro\Model\SubscriptionResponse**](../Model/SubscriptionResponse.md)

### Authorization

[LoginManager](../../README.md#LoginManager)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
