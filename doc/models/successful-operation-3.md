
# Successful Operation 3

*This model accepts additional fields of type unknown.*

## Structure

`SuccessfulOperation3`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `totalElements` | `number` | Required | - |
| `strategyCollections` | [`StrategyCollection[]`](../../doc/models/strategy-collection.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { SuccessfulOperation3 } from 'walmart-apimatic-sdk';

const successfulOperation3: SuccessfulOperation3 = {
  totalElements: 1,
  strategyCollections: [
    {
      repricerStrategy: 'Buy Box Strategy For testing',
      strategyCollectionId: '41678999-a088-4fd8-9eb4-55f8d8ed4ac8',
      enabled: true,
      assignedCount: 1,
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
    },
    {
      repricerStrategy: 'Buy Box Strategy For testing',
      strategyCollectionId: '41678999-a088-4fd8-9eb4-55f8d8ed4ac8',
      enabled: true,
      assignedCount: 1,
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
          strategyType: 'External Price',
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
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

