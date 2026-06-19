
# Promo Discount

*This model accepts additional fields of type unknown.*

## Structure

`PromoDiscount`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sku` | `string` | Required | - |
| `price` | `number` | Required | - |
| `msrp` | `number` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { PromoDiscount } from 'walmart-apimatic-sdk';

const promoDiscount: PromoDiscount = {
  sku: 'SKU00638931255307',
  price: 11,
  msrp: 15,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

