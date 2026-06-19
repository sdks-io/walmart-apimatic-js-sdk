
# Token Api Res

*This model accepts additional fields of type unknown.*

## Structure

`TokenApiRes`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `summary` | `string` | Required | - |
| `value` | [`Value1`](../../doc/models/value-1.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { TokenApiRes } from 'walmart-apimatic-sdk';

const tokenApiRes: TokenApiRes = {
  summary: 'Token API - authorization_code',
  value: {
    accessToken: 'eyJraWQiOiI1MWY3MjM0Ny0wYWY5LTRhZ.....',
    refreshToken: 'APXcIoTpKMH9OQN....',
    tokenType: 'Bearer',
    expiresIn: 900,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

