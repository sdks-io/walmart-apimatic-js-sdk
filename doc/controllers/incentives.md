# Incentives

```ts
const incentivesApi = new IncentivesApi(client);
```

## Class Name

`IncentivesApi`


# Retrieve Price Incentives Data

Retrieves a comprehensive list of all price incentives available for items in your catalog.

The response includes detailed information such as Item ID, Product Name, Product URL, SKU ID, Target Price, current Price, Incentive Type, Incentive Status, Base referral fee, Reduced Referral Fee, Enrollment Type, Inventory count, Enrollment Date (epoch Timestamp), Expiration date (epoch timestamp), Start date (epoch timestamp), and Incentive ID.

For Walmart-funded items, the Target Price, Expiration Date, Start Date, Incentive ID, Reduced Referral Fee, and Enrollment Type will not be displayed (null values). Additionally, Enrollment Type and Date will not be shown for items eligible for Reduced Referral Fee incentives.

For more information and usage examples, refer to the <a href="https://developer.walmart.com/us-marketplace/docs/retrieve-price-incentives-data">Pricing API Guide</a>.

:information_source: **Note** This endpoint does not require authentication.

```ts
async retrievePriceIncentivesData(
  limit: number,
  offset: number,
  sortBy: string,
  sortOrder: string,
  incentiveType: string,
  incentiveStatus: string,
  wmSecAccessToken: string,
  wmConsumerChannelType: string,
  wmQosCorrelationId: string,
  wmSvcName: string,
  accept: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<SuccessfulOperation5>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `limit` | `number` | Query, Required | Specifies the number of items to return. Allowed range is 1 to 200. Default is 25. |
| `offset` | `number` | Query, Required | Specifies the offset of item list to be returned. Minimum offset value is 0. |
| `sortBy` | `string` | Query, Required | Specifies the sort criteria for items. |
| `sortOrder` | `string` | Query, Required | Specifies the sort order for given sort criteria. |
| `incentiveType` | `string` | Query, Required | Specifies the incentive type to filter the incentive items. |
| `incentiveStatus` | `string` | Query, Required | Specifies the incentive status to retrieve items with `ELIGIBLE` or `ENROLLED` incentives. |
| `wmSecAccessToken` | `string` | Header, Required | Access token obtained from the Token API. This is required for authenticating requests to Walmart Marketplace APIs. |
| `wmConsumerChannelType` | `string` | Header, Required | A unique ID to track the consumer request by channel. Use the Consumer Channel Type received during onboarding. |
| `wmQosCorrelationId` | `string` | Header, Required | A unique ID that identifies each API call and is used to track and debug issues. Use a randomly generated GUID for this ID. |
| `wmSvcName` | `string` | Header, Required | Specifies the name of the Walmart service being called. |
| `accept` | `string` | Header, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`SuccessfulOperation5`](../../doc/models/successful-operation-5.md).

## Example Usage

```ts
const limit = 25;

const offset = 0;

const sortBy = 'EXPIRATION_DATE';

const sortOrder = 'DESC';

const incentiveType = 'REDUCED_REFERRAL';

const incentiveStatus = 'ELIGIBLE';

const wmSecAccessToken = 'eyJraWQiOiIzZjVhYTFmNS1hYWE5LTQzM.....';

const wmConsumerChannelType = 'string';

const wmQosCorrelationId = 'b3261d2d-028a-4ef7-8602-633c23200af6';

const wmSvcName = 'Walmart Marketplace';

const accept = 'application/json';

try {
  const response = await incentivesApi.retrievePriceIncentivesData(
    limit,
    offset,
    sortBy,
    sortOrder,
    incentiveType,
    incentiveStatus,
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
  "pageContext": {
    "pageNo": 1,
    "currentPageCount": 1,
    "totalCount": 10,
    "totalPages": 1
  },
  "items": [
    {
      "itemId": "649861121",
      "productName": "Fake Firearm",
      "productUrl": "http://producturl",
      "productImageUrl": "http://imageurl",
      "skuId": "sku123",
      "currentPrice": 20.5,
      "targetPrice": 20,
      "shippingPrice": 2,
      "incentiveType": "REDUCED_REFERRAL",
      "baseReferralFee": 8,
      "reducedReferralFee": 7,
      "enrollmentType": "MANUAL",
      "enrollmentDate": "1652857199000",
      "incentiveStatus": "ELIGIBLE",
      "inventoryCount": 5812.897682047411,
      "startDate": "1660805999000",
      "expirationDate": "1660805999000",
      "incentiveId": "d9c8b7f9-ff0c-461e-8d1f-d3064c156710"
    },
    {
      "itemId": "649861121",
      "productName": "Fake Firearm",
      "productUrl": "http://producturl",
      "productImageUrl": "http://imageurl",
      "skuId": "sku123",
      "currentPrice": 20.5,
      "targetPrice": 20,
      "shippingPrice": 2,
      "incentiveType": "REDUCED_REFERRAL",
      "baseReferralFee": 8,
      "reducedReferralFee": 7,
      "enrollmentType": "MANUAL",
      "enrollmentDate": "1652857199000",
      "incentiveStatus": "ENROLLED",
      "inventoryCount": 850.0178968340776,
      "startDate": "1660805999000",
      "expirationDate": "1660805999000",
      "incentiveId": "d9c8b7f9-ff0c-461e-8d1f-d3064c156710"
    }
  ]
}
```

