# Strategies

```ts
const strategiesApi = new StrategiesApi(client);
```

## Class Name

`StrategiesApi`


# Retrieve Repricer Strategy Details

Retrieves the details of a specific repricer strategy that was previously created for items in Walmart Marketplace.

Use this API to view the list of strategies used and details about the strategy including the strategy collection name, status, assigned items count, and strategy type.

For more information and usage examples, refer to the <a href="https://developer.walmart.com/us-marketplace/docs/get-repricer-strategy">Pricing API Guide</a>.

:information_source: **Note** This endpoint does not require authentication.

```ts
async retrieveRepricerStrategyDetails(
  wmSecAccessToken: string,
  wmConsumerChannelType: string,
  wmQosCorrelationId: string,
  wmSvcName: string,
  accept: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<SuccessfulOperation3>>
```

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

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`SuccessfulOperation3`](../../doc/models/successful-operation-3.md).

## Example Usage

```ts
const wmSecAccessToken = 'eyJraWQiOiIzZjVhYTFmNS1hYWE5LTQzM.....';

const wmConsumerChannelType = 'string';

const wmQosCorrelationId = 'b3261d2d-028a-4ef7-8602-633c23200af6';

const wmSvcName = 'Walmart Marketplace';

const accept = 'application/json';

try {
  const response = await strategiesApi.retrieveRepricerStrategyDetails(
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
  "totalElements": 1,
  "strategyCollections": [
    {
      "repricerStrategy": "Buy Box Strategy For testing",
      "strategyCollectionId": "41678999-a088-4fd8-9eb4-55f8d8ed4ac8",
      "enabled": true,
      "assignedCount": 1,
      "enableRepricerForPromotion": true,
      "restoreSellerPriceWithoutTarget": true,
      "enableBuyboxMeetExternal": true,
      "compareWith3pOfferOnly": true,
      "strategies": [
        {
          "strategyType": "Buy Box Price",
          "adjustmentType": "UNIT",
          "adjustmentValue": 1.2
        },
        {
          "strategyType": "Buy Box Price",
          "adjustmentType": "UNIT",
          "adjustmentValue": 1.2
        }
      ]
    },
    {
      "repricerStrategy": "Buy Box Strategy For testing",
      "strategyCollectionId": "41678999-a088-4fd8-9eb4-55f8d8ed4ac8",
      "enabled": true,
      "assignedCount": 1,
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
          "strategyType": "External Price",
          "adjustmentType": "UNIT",
          "adjustmentValue": 1.2
        }
      ]
    }
  ]
}
```

