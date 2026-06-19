
# Update Pricing for a Single Item Request

*This model accepts additional fields of type unknown.*

## Structure

`UpdatePricingForASingleItemRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sku` | `string` | Required | - |
| `pricing` | [`Pricing[]`](../../doc/models/pricing.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { UpdatePricingForASingleItemRequest } from 'walmart-apimatic-sdk';

const updatePricingForASingleItemRequest: UpdatePricingForASingleItemRequest = {
  sku: '97964_KFTest',
  pricing: [
    {
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
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

