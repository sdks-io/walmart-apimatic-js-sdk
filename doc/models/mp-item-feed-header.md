
# Mp Item Feed Header

*This model accepts additional fields of type unknown.*

## Structure

`MpItemFeedHeader`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `businessUnit` | `string` | Required | - |
| `version` | `string` | Required | - |
| `locale` | `string` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { MpItemFeedHeader } from 'walmart-apimatic-sdk';

const mpItemFeedHeader: MpItemFeedHeader = {
  businessUnit: 'WALMART_US',
  version: '2.0.20240126-12_25_52-api',
  locale: 'en',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

