
# Program Action

*This model accepts additional fields of type unknown.*

## Structure

`ProgramAction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `itemIdentifiers` | [`ItemIdentifiers`](../../doc/models/item-identifiers.md) | Required | - |
| `programs` | [`Programs`](../../doc/models/programs.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ProgramAction } from 'walmart-apimatic-sdk';

const programAction: ProgramAction = {
  itemIdentifiers: {
    sku: 'SKU-121212121212',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  programs: {
    walmartFundedIncentivesEnrollment: {
      walmartFundedIncentivesEnrollment: 'Opt-in',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

