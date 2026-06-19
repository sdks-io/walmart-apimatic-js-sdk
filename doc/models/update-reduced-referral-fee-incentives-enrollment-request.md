
# Update Reduced Referral Fee Incentives Enrollment Request

*This model accepts additional fields of type unknown.*

## Structure

`UpdateReducedReferralFeeIncentivesEnrollmentRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `programActionFeedHeader` | [`ProgramActionFeedHeader`](../../doc/models/program-action-feed-header.md) | Required | - |
| `programAction` | [`ProgramAction1[]`](../../doc/models/program-action-1.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  UpdateReducedReferralFeeIncentivesEnrollmentRequest,
} from 'walmart-apimatic-sdk';

const updateReducedReferralFeeIncentivesEnrollmentRequest: UpdateReducedReferralFeeIncentivesEnrollmentRequest = {
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
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  programAction: [
    {
      itemIdentifiers: {
        sku: 'SKU-121212121212',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      programs: {
        incentivesEnrollment: {
          referralFeeIncentiveEnrollment: 'Y',
          incentiveType: 'The incentive program targeted by this action. For example, Reduced Referral Fee.',
          incentiveId: 'd9c8b7f9-ff0c-461e-8d1f-d3064c156710',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      itemIdentifiers: {
        sku: 'SKU-121212121212',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      programs: {
        incentivesEnrollment: {
          referralFeeIncentiveEnrollment: 'Y',
          incentiveType: 'The incentive program targeted by this action. For example, Reduced Referral Fee.',
          incentiveId: 'd9c8b7f9-ff0c-461e-8d1f-d3064c156710',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

