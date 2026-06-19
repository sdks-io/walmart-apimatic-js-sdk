
# Sort

*This model accepts additional fields of type unknown.*

## Structure

`Sort`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sortField` | `string` | Required | - |
| `sortOrder` | `string` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Sort } from 'walmart-apimatic-sdk';

const sort: Sort = {
  sortField: 'GMVL30D',
  sortOrder: 'DESC',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

