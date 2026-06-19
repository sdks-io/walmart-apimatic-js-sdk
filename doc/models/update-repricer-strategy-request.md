
# Update Repricer Strategy Request

*This model accepts additional fields of type unknown.*

## Structure

`UpdateRepricerStrategyRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `repricerStrategy` | `string` | Required | - |
| `enabled` | `boolean` | Required | - |
| `enableRepricerForPromotion` | `boolean` | Required | - |
| `restoreSellerPriceWithoutTarget` | `boolean` | Required | - |
| `enableBuyboxMeetExternal` | `boolean` | Required | - |
| `compareWith3POfferOnly` | `boolean` | Required | - |
| `strategies` | [`Strategy[]`](../../doc/models/strategy.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { UpdateRepricerStrategyRequest } from 'walmart-apimatic-sdk';

const updateRepricerStrategyRequest: UpdateRepricerStrategyRequest = {
  repricerStrategy: 'Buy Box Strategy',
  enabled: true,
  enableRepricerForPromotion: true,
  restoreSellerPriceWithoutTarget: true,
  enableBuyboxMeetExternal: true,
  compareWith3POfferOnly: true,
  strategies: [
    {
      strategyType: 'Buy Box Price',
      adjustmentType: 'UNIT',
      adjustmentValue: 1.2,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      strategyType: 'Competitive Price',
      adjustmentType: 'UNIT',
      adjustmentValue: 1.2,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

