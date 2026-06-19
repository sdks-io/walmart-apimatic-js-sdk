
# Item 1

*This model accepts additional fields of type unknown.*

## Structure

`Item1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `strategy` | [`Strategy5`](../../doc/models/strategy-5.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Item1 } from 'walmart-apimatic-sdk';

const item1: Item1 = {
  strategy: {
    sku: '06068064605122shoe',
    repricerStrategy: 'Match Competitive Price',
    minimumSellerAllowedPrice: 7.2,
    maximumSellerAllowedPrice: 8,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

