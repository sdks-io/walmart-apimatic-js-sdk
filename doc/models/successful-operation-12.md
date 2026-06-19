
# Successful Operation 12

*This model accepts additional fields of type unknown.*

## Structure

`SuccessfulOperation12`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `martId` | `string` | Required | - |
| `statusInfo` | [`StatusInfo`](../../doc/models/status-info.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { SuccessfulOperation12 } from 'walmart-apimatic-sdk';

const successfulOperation12: SuccessfulOperation12 = {
  martId: 'string',
  statusInfo: {
    subsidyEnrolled: true,
    subsidyPreference: false,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

