
# Successful Operation 4

*This model accepts additional fields of type unknown.*

## Structure

`SuccessfulOperation4`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `autoEnrollEnabled` | `boolean` | Required | - |
| `isDisabled` | `boolean` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { SuccessfulOperation4 } from 'walmart-apimatic-sdk';

const successfulOperation4: SuccessfulOperation4 = {
  autoEnrollEnabled: true,
  isDisabled: true,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

