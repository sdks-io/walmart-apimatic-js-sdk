
# Item Identifiers

*This model accepts additional fields of type unknown.*

## Structure

`ItemIdentifiers`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sku` | `string` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ItemIdentifiers } from 'walmart-apimatic-sdk';

const itemIdentifiers: ItemIdentifiers = {
  sku: 'SKU-121212121212',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

