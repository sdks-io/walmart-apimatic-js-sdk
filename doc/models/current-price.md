
# Current Price

*This model accepts additional fields of type unknown.*

## Structure

`CurrentPrice`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `currency` | `string` | Required | - |
| `amount` | `number` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { CurrentPrice } from 'walmart-apimatic-sdk';

const currentPrice: CurrentPrice = {
  currency: 'USD',
  amount: 10,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

