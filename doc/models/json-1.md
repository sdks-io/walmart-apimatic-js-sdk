
# Json 1

*This model accepts additional fields of type unknown.*

## Structure

`Json1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `feedId` | `string` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Json1 } from 'walmart-apimatic-sdk';

const json1: Json1 = {
  feedId: '14066B6642344B76A8B77AC094F8C63B@AVMBAgA',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

