
# Assign Unassign Items to from Repricer Strategy Request

*This model accepts additional fields of type unknown.*

## Structure

`AssignUnassignItemsToFromRepricerStrategyRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `itemFeedHeader` | [`ItemFeedHeader`](../../doc/models/item-feed-header.md) | Required | - |
| `item` | [`Item1[]`](../../doc/models/item-1.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  AssignUnassignItemsToFromRepricerStrategyRequest,
} from 'walmart-apimatic-sdk';

const assignUnassignItemsToFromRepricerStrategyRequest: AssignUnassignItemsToFromRepricerStrategyRequest = {
  itemFeedHeader: {
    processMode: 'REPLACE',
    subset: 'EXTERNAL',
    mart: 'WALMART_US',
    sellingChannel: 'repricerstrategy',
    version: '1.1',
    locale: 'en',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  item: [
    {
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
    },
    {
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
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

