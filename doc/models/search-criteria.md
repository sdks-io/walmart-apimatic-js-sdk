
# Search Criteria

*This model accepts additional fields of type unknown.*

## Structure

`SearchCriteria`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `searchField` | `string` | Required | - |
| `searchValue` | `string[]` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { SearchCriteria } from 'walmart-apimatic-sdk';

const searchCriteria: SearchCriteria = {
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
};
```

