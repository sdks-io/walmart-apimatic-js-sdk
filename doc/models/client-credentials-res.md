
# Client Credentials Res

*This model accepts additional fields of type unknown.*

## Structure

`ClientCredentialsRes`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `summary` | `string` | Required | - |
| `value` | [`Value`](../../doc/models/value.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { ClientCredentialsRes } from 'walmart-apimatic-sdk';

const clientCredentialsRes: ClientCredentialsRes = {
  summary: 'Token API - client_credentials',
  value: {
    accessToken: 'eyJraWQiOiI1MWY3MjM0Ny0wYWY5LTRhZ.....',
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

