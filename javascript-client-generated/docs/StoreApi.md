# SwaggerPetstore.StoreApi

All URIs are relative to *https://virtserver.swaggerhub.com/TINTACHINA84/PetstoreTemplate/1.0.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteOrder**](StoreApi.md#deleteOrder) | **DELETE** /store/order/{orderId} | Delete purchase order by ID
[**getInventory**](StoreApi.md#getInventory) | **GET** /store/inventory | Returns pet inventories by status
[**getOrderById**](StoreApi.md#getOrderById) | **GET** /store/order/{orderId} | Find purchase order by ID
[**placeOrder**](StoreApi.md#placeOrder) | **POST** /store/order | Place an order for a pet

<a name="deleteOrder"></a>
# **deleteOrder**
> deleteOrder(orderId)

Delete purchase order by ID

For valid response try integer IDs with positive integer value.\\ \\ Negative or non-integer values will generate API errors

### Example
```javascript
import {SwaggerPetstore} from 'swagger_petstore';

let apiInstance = new SwaggerPetstore.StoreApi();
let orderId = 789; // Number | ID of the order that needs to be deleted

apiInstance.deleteOrder(orderId, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | **Number**| ID of the order that needs to be deleted | 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

<a name="getInventory"></a>
# **getInventory**
> {&#x27;String&#x27;: &#x27;Number&#x27;} getInventory()

Returns pet inventories by status

Returns a map of status codes to quantities

### Example
```javascript
import {SwaggerPetstore} from 'swagger_petstore';
let defaultClient = SwaggerPetstore.ApiClient.instance;

// Configure API key authorization: api_key
let api_key = defaultClient.authentications['api_key'];
api_key.apiKey = 'YOUR API KEY';
// Uncomment the following line to set a prefix for the API key, e.g. "Token" (defaults to null)
//api_key.apiKeyPrefix = 'Token';

let apiInstance = new SwaggerPetstore.StoreApi();
apiInstance.getInventory((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters
This endpoint does not need any parameter.

### Return type

**{&#x27;String&#x27;: &#x27;Number&#x27;}**

### Authorization

[api_key](../README.md#api_key)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="getOrderById"></a>
# **getOrderById**
> Order getOrderById(orderId)

Find purchase order by ID

For valid response try integer IDs with value &gt;&#x3D; 1 and &lt;&#x3D; 10.\\ \\ Other values will generated exceptions

### Example
```javascript
import {SwaggerPetstore} from 'swagger_petstore';

let apiInstance = new SwaggerPetstore.StoreApi();
let orderId = 789; // Number | ID of pet that needs to be fetched

apiInstance.getOrderById(orderId, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderId** | **Number**| ID of pet that needs to be fetched | 

### Return type

[**Order**](Order.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

<a name="placeOrder"></a>
# **placeOrder**
> Order placeOrder(body)

Place an order for a pet

### Example
```javascript
import {SwaggerPetstore} from 'swagger_petstore';

let apiInstance = new SwaggerPetstore.StoreApi();
let body = new SwaggerPetstore.Order(); // Order | order placed for purchasing the pet

apiInstance.placeOrder(body, (error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully. Returned data: ' + data);
  }
});
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**Order**](Order.md)| order placed for purchasing the pet | 

### Return type

[**Order**](Order.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json, application/xml

