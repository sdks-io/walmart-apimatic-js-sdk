# Strategy Collection Id

```ts
const mStrategyCollectionIdApi = new MStrategyCollectionIdApi(client);
```

## Class Name

`MStrategyCollectionIdApi`

## Methods

* [Update Repricer Strategy](../../doc/controllers/strategy-collection-id.md#update-repricer-strategy)
* [Delete Repricer Strategy](../../doc/controllers/strategy-collection-id.md#delete-repricer-strategy)


# Update Repricer Strategy

Updates an existing repricer strategy. Use this API to modify and update a repricer strategy rule, name, amount, and unit for a given strategy.

For more information and usage examples, refer to the <a href="https://developer.walmart.com/us-marketplace/docs/update-repricer-strategy">Pricing API Guide</a>.

:information_source: **Note** This endpoint does not require authentication.

```ts
async updateRepricerStrategy(
  strategyCollectionId: string,
  wmSecAccessToken: string,
  wmConsumerChannelType: string,
  wmQosCorrelationId: string,
  wmSvcName: string,
  accept: string,
  body: UpdateRepricerStrategyRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<SuccessfulOperation>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `strategyCollectionId` | `string` | Template, Required | The unique ID of the repricer strategy. This strategy collection ID is used to identify the specific repricer strategy that should be updated. |
| `wmSecAccessToken` | `string` | Header, Required | Access token obtained from the Token API. This is required for authenticating requests to Walmart Marketplace APIs. |
| `wmConsumerChannelType` | `string` | Header, Required | A unique ID to track the consumer request by channel. Use the Consumer Channel Type received during onboarding. |
| `wmQosCorrelationId` | `string` | Header, Required | A unique ID that identifies each API call and is used to track and debug issues. Use a randomly generated GUID for this ID. |
| `wmSvcName` | `string` | Header, Required | Specifies the name of the Walmart service being called. |
| `accept` | `string` | Header, Required | - |
| `body` | [`UpdateRepricerStrategyRequest`](../../doc/models/update-repricer-strategy-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`SuccessfulOperation`](../../doc/models/successful-operation.md).

## Example Usage

```ts
const strategyCollectionId = 'string';

const wmSecAccessToken = 'eyJraWQiOiIzZjVhYTFmNS1hYWE5LTQzM.....';

const wmConsumerChannelType = 'string';

const wmQosCorrelationId = 'b3261d2d-028a-4ef7-8602-633c23200af6';

const wmSvcName = 'Walmart Marketplace';

const accept = 'application/json';

const body: UpdateRepricerStrategyRequest = {
  repricerStrategy: 'Buy Box Strategy',
  enabled: true,
  enableRepricerForPromotion: true,
  restoreSellerPriceWithoutTarget: true,
  enableBuyboxMeetExternal: true,
  compareWith3POfferOnly: true,
  strategies: [
    {
      strategyType: 'Buy Box Price',
      adjustmentType: 'UNIT',
      adjustmentValue: 1.2,
    },
    {
      strategyType: 'Competitive Price',
      adjustmentType: 'UNIT',
      adjustmentValue: 1.2,
    }
  ],
};

try {
  const response = await mStrategyCollectionIdApi.updateRepricerStrategy(
    strategyCollectionId,
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
  "repricerStrategy": "Buy Box Strategy",
  "strategyCollectionId": "41678999-a088-4fd8-9eb4-55f8d8ed4ac8",
  "enabled": true,
  "enableRepricerForPromotion": true,
  "restoreSellerPriceWithoutTarget": true,
  "enableBuyboxMeetExternal": true,
  "compareWith3pOfferOnly": true,
  "strategies": [
    {
      "strategyType": "External Price",
      "adjustmentType": "PERCENTAGE",
      "adjustmentValue": 1.2
    },
    {
      "strategyType": "Buy Box Price",
      "adjustmentType": "UNIT",
      "adjustmentValue": 1.2
    }
  ]
}
```


# Delete Repricer Strategy

Deletes a repricer strategy. Use this API to delete an existing repricer strategy and its corresponding details from the system.

For more information and usage examples, refer to the <a href="https://developer.walmart.com/us-marketplace/docs/delete-repricer-strategy">Pricing API Guide</a>.

:information_source: **Note** This endpoint does not require authentication.

```ts
async deleteRepricerStrategy(
  strategyCollectionId: string,
  wmSecAccessToken: string,
  wmConsumerChannelType: string,
  wmQosCorrelationId: string,
  wmSvcName: string,
  accept: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<SuccessfulOperation1>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `strategyCollectionId` | `string` | Template, Required | The unique ID of the repricer strategy. This strategy collection ID is used to identify the specific repricer strategy that should be deleted. |
| `wmSecAccessToken` | `string` | Header, Required | Access token obtained from the Token API. This is required for authenticating requests to Walmart Marketplace APIs. |
| `wmConsumerChannelType` | `string` | Header, Required | A unique ID to track the consumer request by channel. Use the Consumer Channel Type received during onboarding. |
| `wmQosCorrelationId` | `string` | Header, Required | A unique ID that identifies each API call and is used to track and debug issues. Use a randomly generated GUID for this ID. |
| `wmSvcName` | `string` | Header, Required | Specifies the name of the Walmart service being called. |
| `accept` | `string` | Header, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`SuccessfulOperation1`](../../doc/models/successful-operation-1.md).

## Example Usage

```ts
const strategyCollectionId = 'string';

const wmSecAccessToken = 'eyJraWQiOiIzZjVhYTFmNS1hYWE5LTQzM.....';

const wmConsumerChannelType = 'string';

const wmQosCorrelationId = 'b3261d2d-028a-4ef7-8602-633c23200af6';

const wmSvcName = 'Walmart Marketplace';

const accept = 'application/json';

try {
  const response = await mStrategyCollectionIdApi.deleteRepricerStrategy(
    strategyCollectionId,
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
  "message": "Strategy with Strategy Collection Id : 41678999-a088-4fd8-9eb4-55f8d8ed4ac8 deleted successfully"
}
```

