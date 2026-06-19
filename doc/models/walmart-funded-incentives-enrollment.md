
# Walmart Funded Incentives Enrollment

*This model accepts additional fields of type unknown.*

## Structure

`WalmartFundedIncentivesEnrollment`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `walmartFundedIncentivesEnrollment` | `string` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { WalmartFundedIncentivesEnrollment } from 'walmart-apimatic-sdk';

const walmartFundedIncentivesEnrollment: WalmartFundedIncentivesEnrollment = {
  walmartFundedIncentivesEnrollment: 'Opt-in',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

