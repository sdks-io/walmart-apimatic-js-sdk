
# Successful Operation 8

*This model accepts additional fields of type unknown.*

## Structure

`SuccessfulOperation8`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `feedId` | `string` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { SuccessfulOperation8 } from 'walmart-apimatic-sdk';

const successfulOperation8: SuccessfulOperation8 = {
  feedId: 'AFEE4EEC9C3541B6A7B58E694416EC82@AUoBAwA',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

