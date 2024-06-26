# SwaggerPetstore.UserApi

All URIs are relative to *https://virtserver.swaggerhub.com/TINTACHINA84/PetstoreTemplate/1.0.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createUser**](UserApi.md#createUser) | **POST** /user | Create user
[**createUsersWithArrayInput**](UserApi.md#createUsersWithArrayInput) | **POST** /user/createWithArray | Creates list of users with given input array
[**createUsersWithListInput**](UserApi.md#createUsersWithListInput) | **POST** /user/createWithList | Creates list of users with given input array
[**deleteUser**](UserApi.md#deleteUser) | **DELETE** /user/{username} | Delete user
[**getUserByName**](UserApi.md#getUserByName) | **GET** /user/{username} | Get user by user name
[**loginUser**](UserApi.md#loginUser) | **GET** /user/login | Logs user into the system
[**logoutUser**](UserApi.md#logoutUser) | **GET** /user/logout | Logs out current logged in user session
[**updateUser**](UserApi.md#updateUser) | **PUT** /user/{username} | Updated user

<a name="createUser"></a>
# **createUser**
> createUser(body)

Create user

This can only be done by the logged in user.

### Example
```javascript
import {SwaggerPetstore} from 'swagger_petstore';

let apiInstance = new SwaggerPetstore.UserApi();
let body = new SwaggerPetstore.User(); // User | Created user object

apiInstance.createUser(body, (error, data, response) => {
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
 **body** | [**User**](User.md)| Created user object | 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

<a name="createUsersWithArrayInput"></a>
# **createUsersWithArrayInput**
> createUsersWithArrayInput(body)

Creates list of users with given input array

### Example
```javascript
import {SwaggerPetstore} from 'swagger_petstore';

let apiInstance = new SwaggerPetstore.UserApi();
let body = [new SwaggerPetstore.User()]; // [User] | List of user object

apiInstance.createUsersWithArrayInput(body, (error, data, response) => {
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
 **body** | [**[User]**](User.md)| List of user object | 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

<a name="createUsersWithListInput"></a>
# **createUsersWithListInput**
> createUsersWithListInput(body)

Creates list of users with given input array

### Example
```javascript
import {SwaggerPetstore} from 'swagger_petstore';

let apiInstance = new SwaggerPetstore.UserApi();
let body = [new SwaggerPetstore.User()]; // [User] | List of user object

apiInstance.createUsersWithListInput(body, (error, data, response) => {
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
 **body** | [**[User]**](User.md)| List of user object | 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

<a name="deleteUser"></a>
# **deleteUser**
> deleteUser(username)

Delete user

This can only be done by the logged in user.

### Example
```javascript
import {SwaggerPetstore} from 'swagger_petstore';

let apiInstance = new SwaggerPetstore.UserApi();
let username = "username_example"; // String | The name that needs to be deleted

apiInstance.deleteUser(username, (error, data, response) => {
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
 **username** | **String**| The name that needs to be deleted | 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

<a name="getUserByName"></a>
# **getUserByName**
> User getUserByName(username)

Get user by user name

### Example
```javascript
import {SwaggerPetstore} from 'swagger_petstore';

let apiInstance = new SwaggerPetstore.UserApi();
let username = "username_example"; // String | The name that needs to be fetched. Use user1 for testing.

apiInstance.getUserByName(username, (error, data, response) => {
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
 **username** | **String**| The name that needs to be fetched. Use user1 for testing. | 

### Return type

[**User**](User.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

<a name="loginUser"></a>
# **loginUser**
> &#x27;String&#x27; loginUser(username, password)

Logs user into the system

### Example
```javascript
import {SwaggerPetstore} from 'swagger_petstore';

let apiInstance = new SwaggerPetstore.UserApi();
let username = "username_example"; // String | The user name for login
let password = "password_example"; // String | The password for login in clear text

apiInstance.loginUser(username, password, (error, data, response) => {
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
 **username** | **String**| The user name for login | 
 **password** | **String**| The password for login in clear text | 

### Return type

**&#x27;String&#x27;**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml

<a name="logoutUser"></a>
# **logoutUser**
> logoutUser()

Logs out current logged in user session

### Example
```javascript
import {SwaggerPetstore} from 'swagger_petstore';

let apiInstance = new SwaggerPetstore.UserApi();
apiInstance.logoutUser((error, data, response) => {
  if (error) {
    console.error(error);
  } else {
    console.log('API called successfully.');
  }
});
```

### Parameters
This endpoint does not need any parameter.

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

<a name="updateUser"></a>
# **updateUser**
> updateUser(body, username)

Updated user

This can only be done by the logged in user.

### Example
```javascript
import {SwaggerPetstore} from 'swagger_petstore';

let apiInstance = new SwaggerPetstore.UserApi();
let body = new SwaggerPetstore.User(); // User | Updated user object
let username = "username_example"; // String | name that need to be updated

apiInstance.updateUser(body, username, (error, data, response) => {
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
 **body** | [**User**](User.md)| Updated user object | 
 **username** | **String**| name that need to be updated | 

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

