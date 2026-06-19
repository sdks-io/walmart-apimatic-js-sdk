
# Successful Operation 2

*This model accepts additional fields of type unknown.*

## Structure

`SuccessfulOperation2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `expireAt` | `string` | Required | - |
| `issuedAt` | `string` | Required | - |
| `isValid` | `boolean` | Required | - |
| `scopes` | [`Scopes`](../../doc/models/scopes.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { SuccessfulOperation2 } from 'walmart-apimatic-sdk';

const successfulOperation2: SuccessfulOperation2 = {
  expireAt: '1560973098000',
  issuedAt: '1560972198000',
  isValid: true,
  scopes: {
    reports: 'view_only',
    item: 'full_access',
    price: 'no_access',
    lagtime: 'full_access',
    feeds: 'view_only',
    returns: 'full_access',
    orders: 'full_access',
    inventory: 'full_access',
    content: 'full_access',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

