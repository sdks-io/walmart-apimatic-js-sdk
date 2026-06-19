
# Pricing

*This model accepts additional fields of type unknown.*

## Structure

`Pricing`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `currentPriceType` | `string` | Required | - |
| `currentPrice` | [`CurrentPrice`](../../doc/models/current-price.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Pricing } from 'walmart-apimatic-sdk';

const pricing: Pricing = {
  currentPriceType: 'BASE',
  currentPrice: {
    currency: 'USD',
    amount: 10,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

