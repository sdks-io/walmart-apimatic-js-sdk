
# Item

*This model accepts additional fields of type unknown.*

## Structure

`Item`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `itemId` | `string` | Required | - |
| `productName` | `string` | Required | - |
| `productUrl` | `string` | Required | - |
| `productImageUrl` | `string` | Required | - |
| `skuId` | `string` | Required | - |
| `currentPrice` | `number` | Required | - |
| `targetPrice` | `number` | Required | - |
| `shippingPrice` | `number` | Required | - |
| `incentiveType` | `string` | Required | - |
| `baseReferralFee` | `number` | Required | - |
| `reducedReferralFee` | `number` | Required | - |
| `enrollmentType` | `string` | Required | - |
| `enrollmentDate` | `string` | Required | - |
| `incentiveStatus` | `string` | Required | - |
| `inventoryCount` | `number` | Required | - |
| `startDate` | `string` | Required | - |
| `expirationDate` | `string` | Required | - |
| `incentiveId` | `string` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Item } from 'walmart-apimatic-sdk';

const item: Item = {
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
};
```

