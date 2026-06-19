
# Programs 1

*This model accepts additional fields of type unknown.*

## Structure

`Programs1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `incentivesEnrollment` | [`IncentivesEnrollment`](../../doc/models/incentives-enrollment.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Programs1 } from 'walmart-apimatic-sdk';

const programs1: Programs1 = {
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
};
```

