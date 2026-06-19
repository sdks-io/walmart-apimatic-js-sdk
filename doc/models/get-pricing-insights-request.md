
# Get Pricing Insights Request

*This model accepts additional fields of type unknown.*

## Structure

`GetPricingInsightsRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `filter` | [`Filter[]`](../../doc/models/filter.md) | Required | - |
| `searchCriteria` | [`SearchCriteria`](../../doc/models/search-criteria.md) | Required | - |
| `sort` | [`Sort`](../../doc/models/sort.md) | Required | - |
| `pageNumber` | `number` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { GetPricingInsightsRequest } from 'walmart-apimatic-sdk';

const getPricingInsightsRequest: GetPricingInsightsRequest = {
  filter: [
    {
      name: 'buyBoxWinRate',
      operator: 'BETWEEN',
      value: [
        0,
        75
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      name: 'priceCompetitiveness',
      operator: 'BETWEEN',
      value: [
        0,
        100
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      name: 'gmvL30D',
      operator: 'BETWEEN',
      value: [
        0,
        100
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  searchCriteria: {
    searchField: 'SKU',
    searchValue: [
      '21203526',
      'Candle-lavender-green-tea',
      '504312(1)',
      'hvff'
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  sort: {
    sortField: 'GMVL30D',
    sortOrder: 'DESC',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  pageNumber: 0,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

