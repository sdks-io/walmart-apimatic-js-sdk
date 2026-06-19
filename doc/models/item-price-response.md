
# Item Price Response

*This model accepts additional fields of type unknown.*

## Structure

`ItemPriceResponse`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mart` | `string` | Required | - |
| `message` | `string` | Required | - |
| `sku` | `string` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ItemPriceResponse } from 'walmart-apimatic-sdk';

const itemPriceResponse: ItemPriceResponse = {
  mart: 'WALMART_US',
  message: 'The price of the item has been updated. Allow up to five minutes for this change to be reflected on the Walmart.com.',
  sku: '97964_KFTest',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

