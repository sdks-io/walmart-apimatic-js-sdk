
# Pricing Insights Response List

*This model accepts additional fields of type unknown.*

## Structure

`PricingInsightsResponseList`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `itemName` | `string` | Required | - |
| `sku` | `string` | Required | - |
| `currentPrice` | `number` | Required | - |
| `buyBoxBasePrice` | `number` | Required | - |
| `buyBoxTotalPrice` | `number` | Required | - |
| `buyBoxWinRate` | `string` | Required | - |
| `competitorPrice` | `number` | Required | - |
| `comparisonPrice` | `number` | Required | - |
| `fulfillment` | `string` | Required | - |
| `inventoryCount` | `string \| null` | Required | - |
| `repricerStrategyType` | `string \| null` | Required | - |
| `repricerStrategyName` | `string \| null` | Required | - |
| `repricerStatus` | `string \| null` | Required | - |
| `repricerMinPrice` | `string \| null` | Required | - |
| `repricerMaxPrice` | `string \| null` | Required | - |
| `priceCompetitiveScore` | `number` | Required | - |
| `promoStatus` | `string \| null` | Required | - |
| `potentialGmvLift` | `string \| null` | Required | - |
| `gmv30` | `number` | Required | - |
| `inDemand` | `boolean` | Required | - |
| `priceDifferential` | `string \| null` | Required | - |
| `traffic` | `string \| null` | Required | - |
| `priceCompetitive` | `boolean` | Required | - |
| `reducedReferralStatus` | `string \| null` | Required | - |
| `walmartFundedStatus` | `string` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { PricingInsightsResponseList } from 'walmart-apimatic-sdk';

const pricingInsightsResponseList: PricingInsightsResponseList = {
  itemName: 'Sambazon Sambazon; Inc. Jungle Love Amazon Energy Drink Acai Passion Fruit, 12 oz - Case of 12',
  sku: '21203526',
  currentPrice: 10,
  buyBoxBasePrice: 28.57,
  buyBoxTotalPrice: 44.07,
  buyBoxWinRate: '0.0',
  competitorPrice: 38.17,
  comparisonPrice: 12,
  fulfillment: 'SELLER_FULFILLED',
  inventoryCount: 'inventoryCount6',
  repricerStrategyType: 'repricerStrategyType2',
  repricerStrategyName: 'repricerStrategyName4',
  repricerStatus: 'repricerStatus0',
  repricerMinPrice: 'repricerMinPrice0',
  repricerMaxPrice: 'repricerMaxPrice0',
  priceCompetitiveScore: 0,
  promoStatus: 'promoStatus4',
  potentialGmvLift: 'potentialGmvLift2',
  gmv30: 0,
  inDemand: false,
  priceDifferential: 'priceDifferential2',
  traffic: 'traffic2',
  priceCompetitive: true,
  reducedReferralStatus: 'reducedReferralStatus4',
  walmartFundedStatus: 'INACTIVE_OPT_IN',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

