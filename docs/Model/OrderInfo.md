# # OrderInfo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**shippingAddress** | [**\OpenAPI\Client\Axro\Model\AppSchemasOrderShippingAddressInfo**](AppSchemasOrderShippingAddressInfo.md) |  |
**billingAddress** | [**\OpenAPI\Client\Axro\Model\AppSchemasOrderBillingAddressInfo**](AppSchemasOrderBillingAddressInfo.md) |  |
**cart** | [**\OpenAPI\Client\Axro\Model\CartItemInfo[]**](CartItemInfo.md) |  |
**toll** | **int** |  |
**freightCosts** | **int** |  |
**grandTotal** | **int** |  |
**customReference** | **string** |  | [optional]
**additionalInformation** | **string** |  | [optional]
**orderPlaced** | **bool** |  | [optional] [default to false]
**placeOrderUrl** | **string** |  | [optional] [default to '/api/v1/order/?place=1']

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
