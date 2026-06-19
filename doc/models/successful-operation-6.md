
# Successful Operation 6

*This model accepts additional fields of type unknown.*

## Structure

`SuccessfulOperation6`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pageContext` | [`PageContext`](../../doc/models/page-context.md) | Required | - |
| `pricingInsightsResponseList` | [`PricingInsightsResponseList[]`](../../doc/models/pricing-insights-response-list.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { SuccessfulOperation6 } from 'walmart-apimatic-sdk';

const successfulOperation6: SuccessfulOperation6 = {
  pageContext: {
    pageNo: 0,
    currentPageCount: 0,
    totalCount: 4,
    totalPages: 0,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  pricingInsightsResponseList: [
    {
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
    },
    {
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
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

