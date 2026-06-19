# Repricer Feeds

```ts
const repricerFeedsApi = new RepricerFeedsApi(client);
```

## Class Name

`RepricerFeedsApi`


# Assign Unassign Items to from Repricer Strategy

Adds or removes one or more items from a repricer strategy. Use this API to assign or unassign repricer strategies for items listed in Walmart Marketplace.

In one feed you can update up to 10,000 items in bulk. To ensure optimal feed processing time, we recommend sending no more than 1000 items in one feed and keeping the feed sizes below 10 MB.

For more information and usage examples, refer to the <a href="https://developer.walmart.com/us-marketplace/docs/assign-unassign-items-to-repricer">Pricing API Guide</a>.

:information_source: **Note** This endpoint does not require authentication.

```ts
async assignUnassignItemsToFromRepricerStrategy(
  wmSecAccessToken: string,
  wmConsumerChannelType: string,
  wmQosCorrelationId: string,
  wmSvcName: string,
  accept: string,
  body: AssignUnassignItemsToFromRepricerStrategyRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<SuccessfulOperation8>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `wmSecAccessToken` | `string` | Header, Required | Access token obtained from the Token API. This is required for authenticating requests to Walmart Marketplace APIs. |
| `wmConsumerChannelType` | `string` | Header, Required | A unique ID to track the consumer request by channel. Use the Consumer Channel Type received during onboarding. |
| `wmQosCorrelationId` | `string` | Header, Required | A unique ID that identifies each API call and is used to track and debug issues. Use a randomly generated GUID for this ID. |
| `wmSvcName` | `string` | Header, Required | Specifies the name of the Walmart service being called. |
| `accept` | `string` | Header, Required | - |
| `body` | [`AssignUnassignItemsToFromRepricerStrategyRequest`](../../doc/models/assign-unassign-items-to-from-repricer-strategy-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`SuccessfulOperation8`](../../doc/models/successful-operation-8.md).

## Example Usage

```ts
const wmSecAccessToken = 'eyJraWQiOiIzZjVhYTFmNS1hYWE5LTQzM.....';

const wmConsumerChannelType = 'string';

const wmQosCorrelationId = 'b3261d2d-028a-4ef7-8602-633c23200af6';

const wmSvcName = 'Walmart Marketplace';

const accept = 'application/json';

const body: AssignUnassignItemsToFromRepricerStrategyRequest = {
  itemFeedHeader: {
    processMode: 'REPLACE',
    subset: 'EXTERNAL',
    mart: 'WALMART_US',
    sellingChannel: 'repricerstrategy',
    version: '1.1',
    locale: 'en',
  },
  item: [
    {
      strategy: {
        sku: '06068064605122shoe',
        repricerStrategy: 'Match Competitive Price',
        minimumSellerAllowedPrice: 7.2,
        maximumSellerAllowedPrice: 8,
      },
    },
    {
      strategy: {
        sku: '06068064605122shoe',
        repricerStrategy: 'Match Competitive Price',
        minimumSellerAllowedPrice: 7.2,
        maximumSellerAllowedPrice: 8,
      },
    }
  ],
};

try {
  const response = await repricerFeedsApi.assignUnassignItemsToFromRepricerStrategy(
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
  "feedId": "AFEE4EEC9C3541B6A7B58E694416EC82@AUoBAwA"
}
```

