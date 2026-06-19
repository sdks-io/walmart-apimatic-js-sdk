
# Set Up Cap Sku All Legacy Request

*This model accepts additional fields of type unknown.*

## Structure

`SetUpCapSkuAllLegacyRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `subsidyEnrolled` | `boolean` | Required | - |
| `subsidyPreference` | `boolean` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { SetUpCapSkuAllLegacyRequest } from 'walmart-apimatic-sdk';

const setUpCapSkuAllLegacyRequest: SetUpCapSkuAllLegacyRequest = {
  subsidyEnrolled: false,
  subsidyPreference: true,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

