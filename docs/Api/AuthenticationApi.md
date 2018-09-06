# Swagger\Client\AuthenticationApi

All URIs are relative to *https://mg-eval-test.apigee.net/demo/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**oauthTokenPost**](AuthenticationApi.md#oauthTokenPost) | **POST** /oauth/token | Get Access Token


# **oauthTokenPost**
> \Swagger\Client\Model\AccessToken oauthTokenPost($grant_type, $client_id, $client_secret)

Get Access Token

Verify client credentials and returns a bearer token.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new Swagger\Client\Api\AuthenticationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$grant_type = "client_credentials"; // string | The grant type for OAuth2.0
$client_id = "client_id_example"; // string | Client ID
$client_secret = "client_secret_example"; // string | Client Secret

try {
    $result = $apiInstance->oauthTokenPost($grant_type, $client_id, $client_secret);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthenticationApi->oauthTokenPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **grant_type** | **string**| The grant type for OAuth2.0 | [optional] [default to client_credentials]
 **client_id** | **string**| Client ID | [optional]
 **client_secret** | **string**| Client Secret | [optional]

### Return type

[**\Swagger\Client\Model\AccessToken**](../Model/AccessToken.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

