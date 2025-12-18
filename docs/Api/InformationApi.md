# OpenAPI\Client\Axro\InformationApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getOrderDetailsApiV1InformationOrderDetailOrderNumberGet()**](InformationApi.md#getOrderDetailsApiV1InformationOrderDetailOrderNumberGet) | **GET** /api/v1/information/order/detail/{order_number}/ | Get order details |
| [**getOrderListApiV1InformationOrderListGet()**](InformationApi.md#getOrderListApiV1InformationOrderListGet) | **GET** /api/v1/information/order/list/ | Get order list |
| [**getShipmentDetailsApiV1InformationShipmentDetailShipmentNumberGet()**](InformationApi.md#getShipmentDetailsApiV1InformationShipmentDetailShipmentNumberGet) | **GET** /api/v1/information/shipment/detail/{shipment_number}/ | Get shipment details |
| [**getShipmentListApiV1InformationShipmentListGet()**](InformationApi.md#getShipmentListApiV1InformationShipmentListGet) | **GET** /api/v1/information/shipment/list/ | Get shipment list |
| [**getTrackingHistoryApiV1InformationTrackingHistoryShipmentNumberGet()**](InformationApi.md#getTrackingHistoryApiV1InformationTrackingHistoryShipmentNumberGet) | **GET** /api/v1/information/tracking/history/{shipment_number}/ | Get tracking history |


## `getOrderDetailsApiV1InformationOrderDetailOrderNumberGet()`

```php
getOrderDetailsApiV1InformationOrderDetailOrderNumberGet($orderNumber): \OpenAPI\Client\Axro\Model\OrderDetailsResponse
```

Get order details

Get detailed information about a specific order

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: LoginManager
$config = OpenAPI\Client\Axro\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Axro\Api\InformationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$orderNumber = 'orderNumber_example'; // string

try {
    $result = $apiInstance->getOrderDetailsApiV1InformationOrderDetailOrderNumberGet($orderNumber);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InformationApi->getOrderDetailsApiV1InformationOrderDetailOrderNumberGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **orderNumber** | **string**|  | |

### Return type

[**\OpenAPI\Client\Axro\Model\OrderDetailsResponse**](../Model/OrderDetailsResponse.md)

### Authorization

[LoginManager](../../README.md#LoginManager)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOrderListApiV1InformationOrderListGet()`

```php
getOrderListApiV1InformationOrderListGet($page): \OpenAPI\Client\Axro\Model\OrderListResponse
```

Get order list

Get order list for the current customer

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: LoginManager
$config = OpenAPI\Client\Axro\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Axro\Api\InformationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int | Page number for pagination

try {
    $result = $apiInstance->getOrderListApiV1InformationOrderListGet($page);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InformationApi->getOrderListApiV1InformationOrderListGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| Page number for pagination | [optional] |

### Return type

[**\OpenAPI\Client\Axro\Model\OrderListResponse**](../Model/OrderListResponse.md)

### Authorization

[LoginManager](../../README.md#LoginManager)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getShipmentDetailsApiV1InformationShipmentDetailShipmentNumberGet()`

```php
getShipmentDetailsApiV1InformationShipmentDetailShipmentNumberGet($shipmentNumber): \OpenAPI\Client\Axro\Model\ShipmentDetailsResponse
```

Get shipment details

Get detailed information about a specific shipment

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: LoginManager
$config = OpenAPI\Client\Axro\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Axro\Api\InformationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$shipmentNumber = 'shipmentNumber_example'; // string

try {
    $result = $apiInstance->getShipmentDetailsApiV1InformationShipmentDetailShipmentNumberGet($shipmentNumber);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InformationApi->getShipmentDetailsApiV1InformationShipmentDetailShipmentNumberGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **shipmentNumber** | **string**|  | |

### Return type

[**\OpenAPI\Client\Axro\Model\ShipmentDetailsResponse**](../Model/ShipmentDetailsResponse.md)

### Authorization

[LoginManager](../../README.md#LoginManager)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getShipmentListApiV1InformationShipmentListGet()`

```php
getShipmentListApiV1InformationShipmentListGet($page, $orderNumber): \OpenAPI\Client\Axro\Model\ShipmentListResponse
```

Get shipment list

Get shipment list for the current customer

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: LoginManager
$config = OpenAPI\Client\Axro\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Axro\Api\InformationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int | Page number for pagination
$orderNumber = 'orderNumber_example'; // string | Filter shipments by order number

try {
    $result = $apiInstance->getShipmentListApiV1InformationShipmentListGet($page, $orderNumber);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InformationApi->getShipmentListApiV1InformationShipmentListGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**| Page number for pagination | [optional] |
| **orderNumber** | **string**| Filter shipments by order number | [optional] |

### Return type

[**\OpenAPI\Client\Axro\Model\ShipmentListResponse**](../Model/ShipmentListResponse.md)

### Authorization

[LoginManager](../../README.md#LoginManager)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTrackingHistoryApiV1InformationTrackingHistoryShipmentNumberGet()`

```php
getTrackingHistoryApiV1InformationTrackingHistoryShipmentNumberGet($shipmentNumber): \OpenAPI\Client\Axro\Model\TrackingHistoryResponse
```

Get tracking history

Get ParcelPerform tracking history for a specific shipment

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: LoginManager
$config = OpenAPI\Client\Axro\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Axro\Api\InformationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$shipmentNumber = 'shipmentNumber_example'; // string

try {
    $result = $apiInstance->getTrackingHistoryApiV1InformationTrackingHistoryShipmentNumberGet($shipmentNumber);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InformationApi->getTrackingHistoryApiV1InformationTrackingHistoryShipmentNumberGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **shipmentNumber** | **string**|  | |

### Return type

[**\OpenAPI\Client\Axro\Model\TrackingHistoryResponse**](../Model/TrackingHistoryResponse.md)

### Authorization

[LoginManager](../../README.md#LoginManager)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
