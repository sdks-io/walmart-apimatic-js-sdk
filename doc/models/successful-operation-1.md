
# Successful Operation 1

*This model accepts additional fields of type unknown.*

## Structure

`SuccessfulOperation1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message` | `string` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { SuccessfulOperation1 } from 'walmart-apimatic-sdk';

const successfulOperation1: SuccessfulOperation1 = {
  message: 'Strategy with Strategy Collection Id : 41678999-a088-4fd8-9eb4-55f8d8ed4ac8 deleted successfully',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

