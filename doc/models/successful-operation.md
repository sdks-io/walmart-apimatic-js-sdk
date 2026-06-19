
# Successful Operation

*This model accepts additional fields of type unknown.*

## Structure

`SuccessfulOperation`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `repricerStrategy` | `string` | Required | - |
| `strategyCollectionId` | `string` | Required | - |
| `enabled` | `boolean` | Required | - |
| `enableRepricerForPromotion` | `boolean` | Required | - |
| `restoreSellerPriceWithoutTarget` | `boolean` | Required | - |
| `enableBuyboxMeetExternal` | `boolean` | Required | - |
| `compareWith3POfferOnly` | `boolean` | Required | - |
| `strategies` | [`Strategy[]`](../../doc/models/strategy.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { SuccessfulOperation } from 'walmart-apimatic-sdk';

const successfulOperation: SuccessfulOperation = {
  repricerStrategy: 'Buy Box Strategy',
  strategyCollectionId: '41678999-a088-4fd8-9eb4-55f8d8ed4ac8',
  enabled: true,
  enableRepricerForPromotion: true,
  restoreSellerPriceWithoutTarget: true,
  enableBuyboxMeetExternal: true,
  compareWith3POfferOnly: true,
  strategies: [
    {
      strategyType: 'External Price',
      adjustmentType: 'PERCENTAGE',
      adjustmentValue: 1.2,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      strategyType: 'Buy Box Price',
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

