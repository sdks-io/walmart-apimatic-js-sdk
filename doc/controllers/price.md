# Price

```ts
const priceApi = new PriceApi(client);
```

## Class Name

`PriceApi`


# Update Pricing for a Single Item

Updates the price of an item listed on Walmart Marketplace. Use this API to change the price of a single item. If you want to update pricing for multiple items, we recommend using the <a href="https://developer.walmart.com/us-marketplace/reference/priceandpromotionbulkuploads">Update pricing for multiple items in bulk</a> API.

For more information and usage examples, refer to the <a href="https://developer.walmart.com/us-marketplace/docs/update-pricing-for-a-single-item">Pricing API Guide</a>.

:information_source: **Note** This endpoint does not require authentication.

```ts
async updatePricingForASingleItem(
  wmSecAccessToken: string,
  wmConsumerChannelType: string,
  wmQosCorrelationId: string,
  wmSvcName: string,
  accept: string,
  body: UpdatePricingForASingleItemRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<SuccessfulOperation7>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `wmSecAccessToken` | `string` | Header, Required | Access token obtained from the Token API. This is required for authenticating requests to Walmart Marketplace APIs. |
| `wmConsumerChannelType` | `string` | Header, Required | A unique ID to track the consumer request by channel. Use the Consumer Channel Type received during onboarding. |
| `wmQosCorrelationId` | `string` | Header, Required | A unique ID that identifies each API call and is used to track and debug issues. Use a randomly generated GUID for this ID |
| `wmSvcName` | `string` | Header, Required | Specifies the name of the Walmart service being called. |
| `accept` | `string` | Header, Required | - |
| `body` | [`UpdatePricingForASingleItemRequest`](../../doc/models/update-pricing-for-a-single-item-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`SuccessfulOperation7`](../../doc/models/successful-operation-7.md).

## Example Usage

```ts
const wmSecAccessToken = 'eyJraWQiOiIzZjVhYTFmNS1hYWE5LTQzM.....';

const wmConsumerChannelType = 'string';

const wmQosCorrelationId = 'b3261d2d-028a-4ef7-8602-633c23200af6';

const wmSvcName = 'Walmart Marketplace';

const accept = 'application/json';

const body: UpdatePricingForASingleItemRequest = {
  sku: '97964_KFTest',
  pricing: [
    {
      currentPriceType: 'BASE',
      currentPrice: {
        currency: 'USD',
        amount: 10,
      },
    }
  ],
};

try {
  const response = await priceApi.updatePricingForASingleItem(
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
  "ItemPriceResponse": {
    "mart": "WALMART_US",
    "message": "The price of the item has been updated. Allow up to five minutes for this change to be reflected on the Walmart.com.",
    "sku": "97964_KFTest"
  }
}
```

