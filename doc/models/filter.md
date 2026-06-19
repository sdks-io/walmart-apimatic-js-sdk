
# Filter

*This model accepts additional fields of type unknown.*

## Structure

`Filter`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | - |
| `operator` | `string` | Required | - |
| `value` | `number[]` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Filter } from 'walmart-apimatic-sdk';

const filter: Filter = {
  name: 'buyBoxWinRate',
  operator: 'BETWEEN',
  value: [
    0,
    75
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

