
# Strategy

*This model accepts additional fields of type unknown.*

## Structure

`Strategy`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `strategyType` | `string` | Required | - |
| `adjustmentType` | `string` | Required | - |
| `adjustmentValue` | `number` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Strategy } from 'walmart-apimatic-sdk';

const strategy: Strategy = {
  strategyType: 'Buy Box Price',
  adjustmentType: 'UNIT',
  adjustmentValue: 1.2,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

