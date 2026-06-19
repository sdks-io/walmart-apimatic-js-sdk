
# Successful Operation 5

*This model accepts additional fields of type unknown.*

## Structure

`SuccessfulOperation5`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pageContext` | [`PageContext`](../../doc/models/page-context.md) | Required | - |
| `items` | [`Item[]`](../../doc/models/item.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { SuccessfulOperation5 } from 'walmart-apimatic-sdk';

const successfulOperation5: SuccessfulOperation5 = {
  pageContext: {
    pageNo: 1,
    currentPageCount: 1,
    totalCount: 10,
    totalPages: 1,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  items: [
    {
      itemId: '649861121',
      productName: 'Fake Firearm',
      productUrl: 'http://producturl',
      productImageUrl: 'http://imageurl',
      skuId: 'sku123',
      currentPrice: 20.5,
      targetPrice: 20,
      shippingPrice: 2,
      incentiveType: 'REDUCED_REFERRAL',
      baseReferralFee: 8,
      reducedReferralFee: 7,
      enrollmentType: 'MANUAL',
      enrollmentDate: '1652857199000',
      incentiveStatus: 'ELIGIBLE',
      inventoryCount: 5812.897682047411,
      startDate: '1660805999000',
      expirationDate: '1660805999000',
      incentiveId: 'd9c8b7f9-ff0c-461e-8d1f-d3064c156710',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      itemId: '649861121',
      productName: 'Fake Firearm',
      productUrl: 'http://producturl',
      productImageUrl: 'http://imageurl',
      skuId: 'sku123',
      currentPrice: 20.5,
      targetPrice: 20,
      shippingPrice: 2,
      incentiveType: 'REDUCED_REFERRAL',
      baseReferralFee: 8,
      reducedReferralFee: 7,
      enrollmentType: 'MANUAL',
      enrollmentDate: '1652857199000',
      incentiveStatus: 'ENROLLED',
      inventoryCount: 850.0178968340776,
      startDate: '1660805999000',
      expirationDate: '1660805999000',
      incentiveId: 'd9c8b7f9-ff0c-461e-8d1f-d3064c156710',
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

