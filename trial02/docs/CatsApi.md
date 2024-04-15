# CatsApi

All URIs are relative to *http://catstore.swagger.io/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**listCats**](CatsApi.md#listCats) | **GET** /cats | List all cats |
| [**showCatById**](CatsApi.md#showCatById) | **GET** /cats/{catId} | Info for a specific cat |


<a id="listCats"></a>
# **listCats**
> List&lt;Cat&gt; listCats(limit)

List all cats

### Example
```java
// Import classes:
import com.miyajima.trial.ApiClient;
import com.miyajima.trial.ApiException;
import com.miyajima.trial.Configuration;
import com.miyajima.trial.models.*;
import com.miyajima.trial.api.CatsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://catstore.swagger.io/v1");

    CatsApi apiInstance = new CatsApi(defaultClient);
    Integer limit = 56; // Integer | How many items to return at one time (max 102)
    try {
      List<Cat> result = apiInstance.listCats(limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CatsApi#listCats");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **limit** | **Integer**| How many items to return at one time (max 102) | [optional] |

### Return type

[**List&lt;Cat&gt;**](Cat.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A paged array of cats |  * x-next - A link to the next page of responses <br>  |
| **0** | unexpected error |  -  |

<a id="showCatById"></a>
# **showCatById**
> Cat showCatById(catId)

Info for a specific cat

### Example
```java
// Import classes:
import com.miyajima.trial.ApiClient;
import com.miyajima.trial.ApiException;
import com.miyajima.trial.Configuration;
import com.miyajima.trial.models.*;
import com.miyajima.trial.api.CatsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://catstore.swagger.io/v1");

    CatsApi apiInstance = new CatsApi(defaultClient);
    String catId = "catId_example"; // String | The id of the cat to retrieve
    try {
      Cat result = apiInstance.showCatById(catId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling CatsApi#showCatById");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **catId** | **String**| The id of the cat to retrieve | |

### Return type

[**Cat**](Cat.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | Expected response to a valid request |  -  |
| **0** | unexpected error |  -  |

