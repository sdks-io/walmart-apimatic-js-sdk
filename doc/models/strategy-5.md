
# Strategy 5

*This model accepts additional fields of type unknown.*

## Structure

`Strategy5`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sku` | `string` | Required | - |
| `repricerStrategy` | `string` | Required | - |
| `minimumSellerAllowedPrice` | `number` | Required | - |
| `maximumSellerAllowedPrice` | `number` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Strategy5 } from 'walmart-apimatic-sdk';

const strategy5: Strategy5 = {
  sku: '06068064605122shoe',
  repricerStrategy: 'Match Competitive Price',
  minimumSellerAllowedPrice: 7.2,
  maximumSellerAllowedPrice: 8,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

