
# Programs

*This model accepts additional fields of type unknown.*

## Structure

`Programs`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `walmartFundedIncentivesEnrollment` | [`WalmartFundedIncentivesEnrollment`](../../doc/models/walmart-funded-incentives-enrollment.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Programs } from 'walmart-apimatic-sdk';

const programs: Programs = {
  walmartFundedIncentivesEnrollment: {
    walmartFundedIncentivesEnrollment: 'Opt-in',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

