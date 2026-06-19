
# Successful Operation 11

*This model accepts additional fields of type unknown.*

## Structure

`SuccessfulOperation11`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `feedId` | `string` | Required | - |
| `message` | `string` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { SuccessfulOperation11 } from 'walmart-apimatic-sdk';

const successfulOperation11: SuccessfulOperation11 = {
  feedId: '14066B6642344B76A8B77AC094F8C63B@AVMBAgA',
  message: 'Your items are enrolled in Reduced Referral Fee incentives. Prices will adjust to the incentive thresholds within 4 hours. These incentives will apply until their expiration, but lower prices may continue to apply afterward.',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

