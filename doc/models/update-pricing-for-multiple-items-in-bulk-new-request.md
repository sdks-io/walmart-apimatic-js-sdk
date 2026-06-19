
# Update Pricing for Multiple Items in Bulk New Request

*This model accepts additional fields of type unknown.*

## Structure

`UpdatePricingForMultipleItemsInBulkNewRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mpItemFeedHeader` | [`MpItemFeedHeader`](../../doc/models/mp-item-feed-header.md) | Required | - |
| `mpItem` | [`MpItem[]`](../../doc/models/mp-item.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import {
  UpdatePricingForMultipleItemsInBulkNewRequest,
} from 'walmart-apimatic-sdk';

const updatePricingForMultipleItemsInBulkNewRequest: UpdatePricingForMultipleItemsInBulkNewRequest = {
  mpItemFeedHeader: {
    businessUnit: 'WALMART_US',
    version: '2.0.20240126-12_25_52-api',
    locale: 'en',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  mpItem: [
    {
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
    },
    {
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
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

