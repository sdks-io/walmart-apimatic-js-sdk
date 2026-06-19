
# Program Action 1

*This model accepts additional fields of type unknown.*

## Structure

`ProgramAction1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `itemIdentifiers` | [`ItemIdentifiers`](../../doc/models/item-identifiers.md) | Required | - |
| `programs` | [`Programs1`](../../doc/models/programs-1.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProgramAction1 } from 'walmart-apimatic-sdk';

const programAction1: ProgramAction1 = {
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
};
```

