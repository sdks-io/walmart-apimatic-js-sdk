
# Value

*This model accepts additional fields of type unknown.*

## Structure

`Value`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accessToken` | `string` | Required | - |
| `tokenType` | `string` | Required | - |
| `expiresIn` | `number` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Value } from 'walmart-apimatic-sdk';

const value: Value = {
  accessToken: 'eyJraWQiOiI1MWY3MjM0Ny0wYWY5LTRhZ.....',
  tokenType: 'Bearer',
  expiresIn: 900,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

