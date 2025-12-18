# OpenAPI\Client\Axro\LoginApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**loginApiV1LoginPost()**](LoginApi.md#loginApiV1LoginPost) | **POST** /api/v1/login/ | Login with username and password |


## `loginApiV1LoginPost()`

```php
loginApiV1LoginPost($username, $password): \OpenAPI\Client\Axro\Model\LoginResponse
```

Login with username and password

Login with username and password to get an access token

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Axro\Api\LoginApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$username = 'username_example'; // string
$password = 'password_example'; // string

try {
    $result = $apiInstance->loginApiV1LoginPost($username, $password);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LoginApi->loginApiV1LoginPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**|  | |
| **password** | **string**|  | |

### Return type

[**\OpenAPI\Client\Axro\Model\LoginResponse**](../Model/LoginResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/x-www-form-urlencoded`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
