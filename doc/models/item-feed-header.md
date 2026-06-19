
# Item Feed Header

*This model accepts additional fields of type unknown.*

## Structure

`ItemFeedHeader`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `processMode` | `string` | Required | - |
| `subset` | `string` | Required | - |
| `mart` | `string` | Required | - |
| `sellingChannel` | `string` | Required | - |
| `version` | `string` | Required | - |
| `locale` | `string` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ItemFeedHeader } from 'walmart-apimatic-sdk';

const itemFeedHeader: ItemFeedHeader = {
  processMode: 'REPLACE',
  subset: 'EXTERNAL',
  mart: 'WALMART_US',
  sellingChannel: 'repricerstrategy',
  version: '1.1',
  locale: 'en',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

