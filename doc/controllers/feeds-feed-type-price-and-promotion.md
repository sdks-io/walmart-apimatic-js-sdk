# Feeds ? Feed Type PRICE and PROMOTION

```ts
const feedsFeedTypePriceAndPromotionApi = new FeedsFeedTypePriceAndPromotionApi(client);
```

## Class Name

`FeedsFeedTypePriceAndPromotionApi`


# Update Pricing for Multiple Items in Bulk New

Updates the price and promotions in bulk for multiple items. You can modify the prices of multiple items in bulk using a price feed. This is useful for implementing pricing strategies across your catalog, such as seasonal discounts, competitive pricing adjustments, or clearance sales.

Each price feed can contain up to 10,000 items. To ensure optimal performance (feed processing time), we recommend limiting the feeds to 1,000 items and keeping the payload under 10 MB.

The price sequence guarantee is observed by the bulk price update functionality, subject to the following rules:

Use this API instead of the single price update API, especially if a new item has been set up and a Walmart Part ID (wpid) is available. Ensure to wait at least 24 hours after item creation to use the bulk price update API. The bulk price update Service Level Agreement (SLA) is 15 minutes.

You may include the same Stock Keeping Unit (SKU) multiple times in a single feed. However, if a SKU is repeated in a feed, only on price will be applied. The price sequence guarantee ensures that the latest price update, based on its creation timestamp, is the one that changes the price of the item, overwriting the previous version. Price updates received with an earlier timestamp are ignored. As a result, we recommend all feed-based bulk updates base the value of `feedDate` on UTC.

After submitting the price feed, wait at least 5 minutes before checking whether the bulk price update was successful. If a price update fails, for example due to duplicate SKU entries, an error response will be returned.

For more information and usage examples, refer to the <a href="https://developer.walmart.com/us-marketplace/reference/priceandpromotionbulkuploads">Pricing API Guide</a>.

:information_source: **Note** This endpoint does not require authentication.

```ts
async updatePricingForMultipleItemsInBulkNew(
  feedType: string,
  wmSecAccessToken: string,
  wmConsumerChannelType: string,
  wmQosCorrelationId: string,
  wmSvcName: string,
  accept: string,
  body: UpdatePricingForMultipleItemsInBulkNewRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<SuccessfulOperation8>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `feedType` | `string` | Query, Required | - |
| `wmSecAccessToken` | `string` | Header, Required | Access token obtained from the Token API. This is required for authenticating requests to Walmart Marketplace APIs. |
| `wmConsumerChannelType` | `string` | Header, Required | A unique ID to track the consumer request by channel. Use the Consumer Channel Type received during onboarding. |
| `wmQosCorrelationId` | `string` | Header, Required | A unique ID that identifies each API call and is used to track and debug issues. Use a randomly generated GUID for this ID. |
| `wmSvcName` | `string` | Header, Required | Specifies the name of the Walmart service being called. |
| `accept` | `string` | Header, Required | - |
| `body` | [`UpdatePricingForMultipleItemsInBulkNewRequest`](../../doc/models/update-pricing-for-multiple-items-in-bulk-new-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`SuccessfulOperation8`](../../doc/models/successful-operation-8.md).

## Example Usage

```ts
const feedType = 'PRICE_AND_PROMOTION';

const wmSecAccessToken = 'eyJraWQiOiIzZjVhYTFmNS1hYWE5LTQzM.....';

const wmConsumerChannelType = 'string';

const wmQosCorrelationId = 'b3261d2d-028a-4ef7-8602-633c23200af6';

const wmSvcName = 'Walmart Marketplace';

const accept = 'application/json';

const body: UpdatePricingForMultipleItemsInBulkNewRequest = {
  mpItemFeedHeader: {
    businessUnit: 'WALMART_US',
    version: '2.0.20240126-12_25_52-api',
    locale: 'en',
  },
  mpItem: [
    {
      promoDiscount: {
        sku: 'SKU00638931255307',
        price: 11,
        msrp: 15,
      },
    },
    {
      promoDiscount: {
        sku: 'SKU00638931255307',
        price: 11,
        msrp: 15,
      },
    }
  ],
};

try {
  const response = await feedsFeedTypePriceAndPromotionApi.updatePricingForMultipleItemsInBulkNew(
    feedType,
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
  "feedId": "14066B6642344B76A8B77AC094F8C63B@AVMBAgA"
}
```

