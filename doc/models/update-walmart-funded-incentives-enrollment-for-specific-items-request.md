
# Update Walmart Funded Incentives Enrollment for Specific Items Request

*This model accepts additional fields of type unknown.*

## Structure

`UpdateWalmartFundedIncentivesEnrollmentForSpecificItemsRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `programActionFeedHeader` | [`ProgramActionFeedHeader`](../../doc/models/program-action-feed-header.md) | Required | - |
| `programAction` | [`ProgramAction[]`](../../doc/models/program-action.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  UpdateWalmartFundedIncentivesEnrollmentForSpecificItemsRequest,
} from 'walmart-apimatic-sdk';

const updateWalmartFundedIncentivesEnrollmentForSpecificItemsRequest: UpdateWalmartFundedIncentivesEnrollmentForSpecificItemsRequest = {
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
        walmartFundedIncentivesEnrollment: {
          walmartFundedIncentivesEnrollment: 'Opt-in',
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
        walmartFundedIncentivesEnrollment: {
          walmartFundedIncentivesEnrollment: 'Opt-in',
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

