# Detail

```ts
const detailApi = new DetailApi(client);
```

## Class Name

`DetailApi`


# Token Detail

Returns OAuth token metadata and scopes granted by the seller to your application. Use this to verify whether a token is valid, when it expires, and which API categories are allowed (full_access, view_only, no_access). Send the access token in the `WM_SEC.ACCESS_TOKEN` header.

You can also use this API for troubleshooting access failures and rendering “connected account” permissions in your UI. For more information and usage examples, refer to <a href="https://developer.walmart.com/us-marketplace/docs/retrieve-access-token-details">Retrieve access token details.</a>

```ts
async tokenDetail(
  wmSecAccessToken: string,
  wmConsumerChannelType: string,
  wmQosCorrelationId: string,
  wmSvcName: string,
  accept: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<SuccessfulOperation2>>
```

## Authentication

This endpoint requires [basic](../../doc/auth/basic-authentication.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `wmSecAccessToken` | `string` | Header, Required | Access token obtained from the Token API. This is required for authenticating requests to Walmart Marketplace APIs. |
| `wmConsumerChannelType` | `string` | Header, Required | A unique ID to track the consumer request by channel. Use the Consumer Channel Type received during onboarding. |
| `wmQosCorrelationId` | `string` | Header, Required | A unique ID that identifies each API call and is used to track and debug issues. Use a randomly generated GUID for this ID. |
| `wmSvcName` | `string` | Header, Required | Specifies the name of the Walmart service being called. |
| `accept` | `string` | Header, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`SuccessfulOperation2`](../../doc/models/successful-operation-2.md).

## Example Usage

```ts
const wmSecAccessToken = 'eyJraWQiOiIzZjVhYTFmNS1hYWE5LTQzM.....';

const wmConsumerChannelType = 'string';

const wmQosCorrelationId = 'b3261d2d-028a-4ef7-8602-633c23200af6';

const wmSvcName = 'Walmart Marketplace';

const accept = 'application/json';

try {
  const response = await detailApi.tokenDetail(
    wmSecAccessToken,
    wmConsumerChannelType,
    wmQosCorrelationId,
    wmSvcName,
    accept
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

## Example Response *(as JSON)*

```json
{
  "expire_at": "1560973098000",
  "issued_at": "1560972198000",
  "is_valid": true,
  "scopes": {
    "reports": "view_only",
    "item": "full_access",
    "price": "no_access",
    "lagtime": "full_access",
    "feeds": "view_only",
    "returns": "full_access",
    "orders": "full_access",
    "inventory": "full_access",
    "content": "full_access"
  }
}
```

