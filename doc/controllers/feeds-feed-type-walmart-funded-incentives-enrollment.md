# Feeds ? Feed Type WALMART FUNDED INCENTIVES ENROLLMENT

```ts
const feedsFeedTypeWalmartFundedIncentivesEnrollmentApi = new FeedsFeedTypeWalmartFundedIncentivesEnrollmentApi(client);
```

## Class Name

`FeedsFeedTypeWalmartFundedIncentivesEnrollmentApi`


# Update Walmart-Funded Incentives Enrollment for Specific Items

Updates the enrollment status of specific items in the Walmart-funded incentives program. By default, all items are auto-enrolled in Walmart-funded incentives, meaning that eligible items are automatically included in this program to benefit from price reductions funded by Walmart.

You have the flexibility to modify the enrollment status for specific items using this API: <ul><li>Opt-Out - Use this option to opt-out of Walmart-funded incentives for specific items for which you do not want to lower the price.</li> <li>Opt-in - Use this option to opt-in items that were previously opted-out from Walmart-funded incentives. For instance, you can re-enroll items in Walmart-funded incentives programs at any time depending on your business needs.</li></ul>

For more information and usage examples, refer to the <a href="https://developer.walmart.com/us-marketplace/docs/manage-enrollment-specific-items-in-walmart-funded-incentives">Pricing API Guide</a>.

:information_source: **Note** This endpoint does not require authentication.

```ts
async updateWalmartFundedIncentivesEnrollmentForSpecificItems(
  feedType: string,
  wmSecAccessToken: string,
  wmConsumerChannelType: string,
  wmQosCorrelationId: string,
  wmSvcName: string,
  accept: string,
  body: UpdateWalmartFundedIncentivesEnrollmentForSpecificItemsRequest,
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
| `body` | [`UpdateWalmartFundedIncentivesEnrollmentForSpecificItemsRequest`](../../doc/models/update-walmart-funded-incentives-enrollment-for-specific-items-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`SuccessfulOperation8`](../../doc/models/successful-operation-8.md).

## Example Usage

```ts
const feedType = 'WALMART_FUNDED_INCENTIVES_ENROLLMENT';

const wmSecAccessToken = 'eyJraWQiOiIzZjVhYTFmNS1hYWE5LTQzM.....';

const wmConsumerChannelType = 'string';

const wmQosCorrelationId = 'b3261d2d-028a-4ef7-8602-633c23200af6';

const wmSvcName = 'Walmart Marketplace';

const accept = 'application/json';

const body: UpdateWalmartFundedIncentivesEnrollmentForSpecificItemsRequest = {
  programActionFeedHeader: {
    requestId: '0a90b332-1f92-40f4-afb1-92301f5d828e',
    requestBatchId: '0a90b332-1f92-40f4-afb1-92301f5d828e',
    processMode: 'REPLACE',
    subset: 'EXTERNAL',
    sellingChannel: 'online',
    version: '5.0.20240805-15_25_31',
    locale: 'en',
    feedDate: '2024-07-11T00:29:58Z',
    feedType: 'PROGRAM_ACTIONS',
  },
  programAction: [
    {
      itemIdentifiers: {
        sku: 'SKU-121212121212',
      },
      programs: {
        walmartFundedIncentivesEnrollment: {
          walmartFundedIncentivesEnrollment: 'Opt-in',
        },
      },
    },
    {
      itemIdentifiers: {
        sku: 'SKU-121212121212',
      },
      programs: {
        walmartFundedIncentivesEnrollment: {
          walmartFundedIncentivesEnrollment: 'Opt-in',
        },
      },
    }
  ],
};

try {
  const response = await feedsFeedTypeWalmartFundedIncentivesEnrollmentApi.updateWalmartFundedIncentivesEnrollmentForSpecificItems(
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

