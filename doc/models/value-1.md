
# Value 1

*This model accepts additional fields of type unknown.*

## Structure

`Value1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `accessToken` | `string` | Required | - |
| `refreshToken` | `string` | Required | - |
| `tokenType` | `string` | Required | - |
| `expiresIn` | `number` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Value1 } from 'walmart-apimatic-sdk';

const value1: Value1 = {
  accessToken: 'eyJraWQiOiI1MWY3MjM0Ny0wYWY5LTRhZ.....',
  refreshToken: 'APXcIoTpKMH9OQN....',
  tokenType: 'Bearer',
  expiresIn: 900,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

