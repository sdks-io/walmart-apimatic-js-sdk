
# Mp Item

*This model accepts additional fields of type unknown.*

## Structure

`MpItem`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `promoDiscount` | [`PromoDiscount`](../../doc/models/promo-discount.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { MpItem } from 'walmart-apimatic-sdk';

const mpItem: MpItem = {
  promoDiscount: {
    sku: 'SKU00638931255307',
    price: 11,
    msrp: 15,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

