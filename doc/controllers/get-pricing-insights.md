# Get Pricing Insights

```ts
const getPricingInsightsApi = new GetPricingInsightsApi(client);
```

## Class Name

`GetPricingInsightsApi`


# Get Pricing Insights

Retrieve pricing insights with filters, sorting, and pagination.Use this API to get comprehensive pricing insights for your items on Walmart Marketplace. You can query your catalog for various pricing attributes, including current price, Buy Box pricing information, competitive pricing information, repricer details, and more.

:information_source: **Note** This endpoint does not require authentication.

```ts
async getPricingInsights(
  wmSecAccessToken: string,
  wmConsumerChannelType: string,
  wmQosCorrelationId: string,
  wmSvcName: string,
  accept: string,
  body: GetPricingInsightsRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<SuccessfulOperation6>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `wmSecAccessToken` | `string` | Header, Required | Access token obtained from the Token API. This is required for authenticating requests to Walmart Marketplace APIs. |
| `wmConsumerChannelType` | `string` | Header, Required | A unique ID to identify the consumer request by channel. Use the Consumer Channel Type received during onboarding. |
| `wmQosCorrelationId` | `string` | Header, Required | A unique ID that identifies each API call and is used to track and debug issues. Use a randomly generated GUID for this ID. |
| `wmSvcName` | `string` | Header, Required | Specifies the name of the Walmart service being called. |
| `accept` | `string` | Header, Required | - |
| `body` | [`GetPricingInsightsRequest`](../../doc/models/get-pricing-insights-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`SuccessfulOperation6`](../../doc/models/successful-operation-6.md).

## Example Usage

```ts
const wmSecAccessToken = 'eyJraWQiOiIxNWNhNGIyYi0yODVjLTQ0ZDUtYmExNC05ZDk1NTlkZmUwNjgiLCJlbmMiOiJBMjU2R0NNIiwiYWxnIjoiZGlyIn0....';

const wmConsumerChannelType = 'string';

const wmQosCorrelationId = 'b3261d2d-028a-4ef7-8602-633c23200af6';

const wmSvcName = 'Walmart Marketplace';

const accept = 'application/json';

const body: GetPricingInsightsRequest = {
  filter: [
    {
      name: 'buyBoxWinRate',
      operator: 'BETWEEN',
      value: [
        0,
        75
      ],
    },
    {
      name: 'priceCompetitiveness',
      operator: 'BETWEEN',
      value: [
        0,
        100
      ],
    },
    {
      name: 'gmvL30D',
      operator: 'BETWEEN',
      value: [
        0,
        100
      ],
    }
  ],
  searchCriteria: {
    searchField: 'SKU',
    searchValue: [
      '21203526',
      'Candle-lavender-green-tea',
      '504312(1)',
      'hvff'
    ],
  },
  sort: {
    sortField: 'GMVL30D',
    sortOrder: 'DESC',
  },
  pageNumber: 0,
};

try {
  const response = await getPricingInsightsApi.getPricingInsights(
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
  "pageContext": {
    "pageNo": 0,
    "currentPageCount": 0,
    "totalCount": 4,
    "totalPages": 0
  },
  "pricingInsightsResponseList": [
    {
      "itemName": "Sambazon Sambazon; Inc. Jungle Love Amazon Energy Drink Acai Passion Fruit, 12 oz - Case of 12",
      "sku": "21203526",
      "currentPrice": 10,
      "buyBoxBasePrice": 28.57,
      "buyBoxTotalPrice": 44.07,
      "buyBoxWinRate": "0.0",
      "competitorPrice": 38.17,
      "comparisonPrice": 12,
      "fulfillment": "SELLER_FULFILLED",
      "inventoryCount": null,
      "repricerStrategyType": null,
      "repricerStrategyName": null,
      "repricerStatus": null,
      "repricerMinPrice": null,
      "repricerMaxPrice": null,
      "priceCompetitiveScore": 0,
      "promoStatus": null,
      "potentialGmvLift": null,
      "gmv30": 0,
      "inDemand": false,
      "priceDifferential": null,
      "traffic": null,
      "priceCompetitive": true,
      "reducedReferralStatus": null,
      "walmartFundedStatus": "INACTIVE_OPT_IN"
    },
    {
      "itemName": "Sambazon Sambazon; Inc. Jungle Love Amazon Energy Drink Acai Passion Fruit, 12 oz - Case of 12",
      "sku": "21203526",
      "currentPrice": 10,
      "buyBoxBasePrice": 28.57,
      "buyBoxTotalPrice": 44.07,
      "buyBoxWinRate": "0.0",
      "competitorPrice": 38.17,
      "comparisonPrice": 12,
      "fulfillment": "SELLER_FULFILLED",
      "inventoryCount": null,
      "repricerStrategyType": null,
      "repricerStrategyName": null,
      "repricerStatus": null,
      "repricerMinPrice": null,
      "repricerMaxPrice": null,
      "priceCompetitiveScore": 0,
      "promoStatus": null,
      "potentialGmvLift": null,
      "gmv30": 0,
      "inDemand": false,
      "priceDifferential": null,
      "traffic": null,
      "priceCompetitive": true,
      "reducedReferralStatus": null,
      "walmartFundedStatus": "INACTIVE_OPT_IN"
    }
  ]
}
```

