# DocsApi

All URIs are relative to *http://docstore.swagger.io/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**listDocs**](DocsApi.md#listDocs) | **GET** /docs | List all docs |
| [**showDocById**](DocsApi.md#showDocById) | **GET** /docs/{docId} | Info for a specific doc |


<a id="listDocs"></a>
# **listDocs**
> List&lt;Doc&gt; listDocs(xRequestId, limit)

List all docs

### Example
```java
// Import classes:
import com.miyajima.trial01.ApiClient;
import com.miyajima.trial01.ApiException;
import com.miyajima.trial01.Configuration;
import com.miyajima.trial01.models.*;
import com.miyajima.trial01.api.DocsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://docstore.swagger.io/v1");

    DocsApi apiInstance = new DocsApi(defaultClient);
    UUID xRequestId = UUID.randomUUID(); // UUID | 
    Integer limit = 56; // Integer | How many items to return at one time (max 102)
    try {
      List<Doc> result = apiInstance.listDocs(xRequestId, limit);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocsApi#listDocs");
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
| **xRequestId** | **UUID**|  | |
| **limit** | **Integer**| How many items to return at one time (max 102) | [optional] |

### Return type

[**List&lt;Doc&gt;**](Doc.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | A paged array of docs |  * x-next - A link to the next page of responses <br>  |
| **0** | unexpected error |  -  |

<a id="showDocById"></a>
# **showDocById**
> Doc showDocById(xRequestId, docId)

Info for a specific doc

### Example
```java
// Import classes:
import com.miyajima.trial01.ApiClient;
import com.miyajima.trial01.ApiException;
import com.miyajima.trial01.Configuration;
import com.miyajima.trial01.models.*;
import com.miyajima.trial01.api.DocsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://docstore.swagger.io/v1");

    DocsApi apiInstance = new DocsApi(defaultClient);
    UUID xRequestId = UUID.randomUUID(); // UUID | 
    String docId = "docId_example"; // String | The id of the doc to retrieve
    try {
      Doc result = apiInstance.showDocById(xRequestId, docId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocsApi#showDocById");
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
| **xRequestId** | **UUID**|  | |
| **docId** | **String**| The id of the doc to retrieve | |

### Return type

[**Doc**](Doc.md)

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

