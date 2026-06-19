# Cppreference

```ts
const cppreferenceApi = new CppreferenceApi(client);
```

## Class Name

`CppreferenceApi`


# Set Up CAP SKU All Legacy

This API helps Sellers to completely opt-in or opt-out from CAP program.

If the subsidyEnrolled value = "true", the Seller enrolls in the CAP program. All eligible SKUs (current and future) are by default opt-in. Seller should use the SKU opt-in/opt-out API to opt-out individual items.

If the subsidyEnrolled value = "false", the Seller stops participating in the CAP program and all eligible SKUs (current and future) are opt-out of the CAP program.

:information_source: **Note** This endpoint does not require authentication.

```ts
async setUpCapSkuAllLegacy(
  wmSecAccessToken: string,
  wmConsumerChannelType: string,
  wmQosCorrelationId: string,
  wmSvcName: string,
  accept: string,
  body: SetUpCapSkuAllLegacyRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<SuccessfulOperation12>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `wmSecAccessToken` | `string` | Header, Required | The access token retrieved in the Token API call |
| `wmConsumerChannelType` | `string` | Header, Required | A unique ID to track the consumer request by channel. Use the Consumer Channel Type received during onboarding |
| `wmQosCorrelationId` | `string` | Header, Required | A unique ID which identifies each API call and used to track and debug issues; use a random generated GUID for this ID |
| `wmSvcName` | `string` | Header, Required | Walmart Service Name |
| `accept` | `string` | Header, Required | - |
| `body` | [`SetUpCapSkuAllLegacyRequest`](../../doc/models/set-up-cap-sku-all-legacy-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`SuccessfulOperation12`](../../doc/models/successful-operation-12.md).

## Example Usage

```ts
const wmSecAccessToken = 'eyJraWQiOiIzZjVhYTFmNS1hYWE5LTQzM.....';

const wmConsumerChannelType = 'string';

const wmQosCorrelationId = 'b3261d2d-028a-4ef7-8602-633c23200af6';

const wmSvcName = 'Walmart Service Name';

const accept = 'application/json';

const body: SetUpCapSkuAllLegacyRequest = {
  subsidyEnrolled: false,
  subsidyPreference: true,
};

try {
  const response = await cppreferenceApi.setUpCapSkuAllLegacy(
    wmSecAccessToken,
    wmConsumerChannelType,
    wmQosCorrelationId,
    wmSvcName,
    accept,
    body
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
  "martId": "string",
  "statusInfo": {
    "subsidyEnrolled": true,
    "subsidyPreference": false
  }
}
```

