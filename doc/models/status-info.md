
# Status Info

*This model accepts additional fields of type unknown.*

## Structure

`StatusInfo`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `subsidyEnrolled` | `boolean` | Required | - |
| `subsidyPreference` | `boolean` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { StatusInfo } from 'walmart-apimatic-sdk';

const statusInfo: StatusInfo = {
  subsidyEnrolled: true,
  subsidyPreference: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

