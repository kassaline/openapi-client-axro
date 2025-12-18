# OpenAPI\Client\Axro\UserApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**readUsersMeApiV1UserInfoGet()**](UserApi.md#readUsersMeApiV1UserInfoGet) | **GET** /api/v1/user/info/ | Get user information |


## `readUsersMeApiV1UserInfoGet()`

```php
readUsersMeApiV1UserInfoGet(): \OpenAPI\Client\Axro\Model\User
```

Get user information

Get user information for the current user

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: LoginManager
$config = OpenAPI\Client\Axro\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Axro\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->readUsersMeApiV1UserInfoGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->readUsersMeApiV1UserInfoGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Axro\Model\User**](../Model/User.md)

### Authorization

[LoginManager](../../README.md#LoginManager)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
