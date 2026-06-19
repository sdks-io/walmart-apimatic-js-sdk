# Feeds ? Feed Type INCENTIVE ENROLLMENT

```ts
const feedsFeedTypeIncentiveEnrollmentApi = new FeedsFeedTypeIncentiveEnrollmentApi(client);
```

## Class Name

`FeedsFeedTypeIncentiveEnrollmentApi`


# Update Reduced Referral Fee Incentives Enrollment

You can use this API endpoint to enroll any eligible item to Reduced Referral Fee incentive. You can also use this endpoint to unenroll any items from active Reduced Referral Fee incentives.

For more information and usage examples, refer to the <a href="https://developer.walmart.com/us-marketplace/docs/enroll-in-reduced-referral-fee-incentives">Pricing API Guide</a>.

:information_source: **Note** This endpoint does not require authentication.

```ts
async updateReducedReferralFeeIncentivesEnrollment(
  feedType: string,
  wmSecAccessToken: string,
  wmConsumerChannelType: string,
  wmQosCorrelationId: string,
  wmSvcName: string,
  accept: string,
  body: UpdateReducedReferralFeeIncentivesEnrollmentRequest,
  requestOptions?: RequestOptions
): Promise<ApiResponse<SuccessfulOperation11>>
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
| `body` | [`UpdateReducedReferralFeeIncentivesEnrollmentRequest`](../../doc/models/update-reduced-referral-fee-incentives-enrollment-request.md) | Body, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`SuccessfulOperation11`](../../doc/models/successful-operation-11.md).

## Example Usage

```ts
const feedType = 'INCENTIVE_ENROLLMENT';

const wmSecAccessToken = 'eyJraWQiOiIzZjVhYTFmNS1hYWE5LTQzM.....';

const wmConsumerChannelType = 'string';

const wmQosCorrelationId = 'b3261d2d-028a-4ef7-8602-633c23200af6';

const wmSvcName = 'Walmart Marketplace';

const accept = 'application/json';

const body: UpdateReducedReferralFeeIncentivesEnrollmentRequest = {
  programActionFeedHeader: {
    requestId: '0a90b332-1f92-40f4-afb1-92301f5d828e',
    requestBatchId: '0a90b332-1f92-40f4-afb1-92301f5d828e',
    processMode: 'REPLACE',
    subset: 'EXTERNAL',
    sellingChannel: 'online',
    version: '5.0.20250322-01_07_46',
    locale: 'en',
    feedDate: '2024-07-11T00:29:58Z',
    feedType: 'INCENTIVE_ENROLLMENT',
  },
  programAction: [
    {
      itemIdentifiers: {
        sku: 'SKU-121212121212',
      },
      programs: {
        incentivesEnrollment: {
          referralFeeIncentiveEnrollment: 'Y',
          incentiveType: 'The incentive program targeted by this action. For example, Reduced Referral Fee.',
          incentiveId: 'd9c8b7f9-ff0c-461e-8d1f-d3064c156710',
        },
      },
    },
    {
      itemIdentifiers: {
        sku: 'SKU-121212121212',
      },
      programs: {
        incentivesEnrollment: {
          referralFeeIncentiveEnrollment: 'Y',
          incentiveType: 'The incentive program targeted by this action. For example, Reduced Referral Fee.',
          incentiveId: 'd9c8b7f9-ff0c-461e-8d1f-d3064c156710',
        },
      },
    }
  ],
};

try {
  const response = await feedsFeedTypeIncentiveEnrollmentApi.updateReducedReferralFeeIncentivesEnrollment(
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
  "feedId": "14066B6642344B76A8B77AC094F8C63B@AVMBAgA",
  "message": "Your items are enrolled in Reduced Referral Fee incentives. Prices will adjust to the incentive thresholds within 4 hours. These incentives will apply until their expiration, but lower prices may continue to apply afterward."
}
```

