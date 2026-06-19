
# Page Context

*This model accepts additional fields of type unknown.*

## Structure

`PageContext`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pageNo` | `number` | Required | - |
| `currentPageCount` | `number` | Required | - |
| `totalCount` | `number` | Required | - |
| `totalPages` | `number` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { PageContext } from 'walmart-apimatic-sdk';

const pageContext: PageContext = {
  pageNo: 1,
  currentPageCount: 1,
  totalCount: 10,
  totalPages: 1,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

