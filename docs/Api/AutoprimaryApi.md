# Swagger\Client\AutoprimaryApi

All URIs are relative to *https://localhost/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**createAutoprimary**](AutoprimaryApi.md#createAutoprimary) | **POST** /servers/{server_id}/autoprimaries | Add an autoprimary
[**deleteAutoprimary**](AutoprimaryApi.md#deleteAutoprimary) | **DELETE** /servers/{server_id}/autoprimaries/{ip}/{nameserver} | Delete the autoprimary entry
[**getAutoprimaries**](AutoprimaryApi.md#getAutoprimaries) | **GET** /servers/{server_id}/autoprimaries | Get a list of autoprimaries


# **createAutoprimary**
> createAutoprimary($server_id, $autoprimary)

Add an autoprimary

This methods add a new autoprimary server.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

$apiInstance = new Swagger\Client\Api\AutoprimaryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$server_id = "server_id_example"; // string | The id of the server to manage the list of autoprimaries on
$autoprimary = new \Swagger\Client\Model\Autoprimary(); // \Swagger\Client\Model\Autoprimary | autoprimary entry to add

try {
    $apiInstance->createAutoprimary($server_id, $autoprimary);
} catch (Exception $e) {
    echo 'Exception when calling AutoprimaryApi->createAutoprimary: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **string**| The id of the server to manage the list of autoprimaries on |
 **autoprimary** | [**\Swagger\Client\Model\Autoprimary**](../Model/Autoprimary.md)| autoprimary entry to add |

### Return type

void (empty response body)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **deleteAutoprimary**
> deleteAutoprimary($server_id, $ip, $nameserver)

Delete the autoprimary entry

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

$apiInstance = new Swagger\Client\Api\AutoprimaryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$server_id = "server_id_example"; // string | The id of the server to delete the autoprimary from
$ip = "ip_example"; // string | IP address of autoprimary
$nameserver = "nameserver_example"; // string | DNS name of the autoprimary

try {
    $apiInstance->deleteAutoprimary($server_id, $ip, $nameserver);
} catch (Exception $e) {
    echo 'Exception when calling AutoprimaryApi->deleteAutoprimary: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **string**| The id of the server to delete the autoprimary from |
 **ip** | **string**| IP address of autoprimary |
 **nameserver** | **string**| DNS name of the autoprimary |

### Return type

void (empty response body)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **getAutoprimaries**
> \Swagger\Client\Model\Autoprimary getAutoprimaries($server_id)

Get a list of autoprimaries

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: APIKeyHeader
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('X-API-Key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-API-Key', 'Bearer');

$apiInstance = new Swagger\Client\Api\AutoprimaryApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$server_id = "server_id_example"; // string | The id of the server to manage the list of autoprimaries on

try {
    $result = $apiInstance->getAutoprimaries($server_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AutoprimaryApi->getAutoprimaries: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **server_id** | **string**| The id of the server to manage the list of autoprimaries on |

### Return type

[**\Swagger\Client\Model\Autoprimary**](../Model/Autoprimary.md)

### Authorization

[APIKeyHeader](../../README.md#APIKeyHeader)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

