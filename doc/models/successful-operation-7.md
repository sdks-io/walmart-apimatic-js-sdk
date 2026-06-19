
# Successful Operation 7

*This model accepts additional fields of type unknown.*

## Structure

`SuccessfulOperation7`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `itemPriceResponse` | [`ItemPriceResponse`](../../doc/models/item-price-response.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { SuccessfulOperation7 } from 'walmart-apimatic-sdk';

const successfulOperation7: SuccessfulOperation7 = {
  itemPriceResponse: {
    mart: 'WALMART_US',
    message: 'The price of the item has been updated. Allow up to five minutes for this change to be reflected on the Walmart.com.',
    sku: '97964_KFTest',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

