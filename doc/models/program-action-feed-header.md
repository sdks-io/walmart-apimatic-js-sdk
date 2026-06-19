
# Program Action Feed Header

*This model accepts additional fields of type unknown.*

## Structure

`ProgramActionFeedHeader`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `requestId` | `string` | Required | - |
| `requestBatchId` | `string` | Required | - |
| `processMode` | `string` | Required | - |
| `subset` | `string` | Required | - |
| `sellingChannel` | `string` | Required | - |
| `version` | `string` | Required | - |
| `locale` | `string` | Required | - |
| `feedDate` | `string` | Required | - |
| `feedType` | `string` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProgramActionFeedHeader } from 'walmart-apimatic-sdk';

const programActionFeedHeader: ProgramActionFeedHeader = {
  requestId: '0a90b332-1f92-40f4-afb1-92301f5d828e',
  requestBatchId: '0a90b332-1f92-40f4-afb1-92301f5d828e',
  processMode: 'REPLACE',
  subset: 'EXTERNAL',
  sellingChannel: 'online',
  version: '5.0.20240805-15_25_31',
  locale: 'en',
  feedDate: '2024-07-11T00:29:58Z',
  feedType: 'PROGRAM_ACTIONS',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

