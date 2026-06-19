
# Incentives Enrollment

*This model accepts additional fields of type unknown.*

## Structure

`IncentivesEnrollment`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `referralFeeIncentiveEnrollment` | `string` | Required | - |
| `incentiveType` | `string` | Required | - |
| `incentiveId` | `string` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { IncentivesEnrollment } from 'walmart-apimatic-sdk';

const incentivesEnrollment: IncentivesEnrollment = {
  referralFeeIncentiveEnrollment: 'Y',
  incentiveType: 'The incentive program targeted by this action. For example, Reduced Referral Fee.',
  incentiveId: 'd9c8b7f9-ff0c-461e-8d1f-d3064c156710',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

