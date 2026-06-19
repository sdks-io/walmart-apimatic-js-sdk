
# Scopes

*This model accepts additional fields of type unknown.*

## Structure

`Scopes`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `reports` | `string` | Required | - |
| `item` | `string` | Required | - |
| `price` | `string` | Required | - |
| `lagtime` | `string` | Required | - |
| `feeds` | `string` | Required | - |
| `returns` | `string` | Required | - |
| `orders` | `string` | Required | - |
| `inventory` | `string` | Required | - |
| `content` | `string` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { Scopes } from 'walmart-apimatic-sdk';

const scopes: Scopes = {
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
};
```

