
# Token Api Authorization Code

*This model accepts additional fields of type unknown.*

## Structure

`TokenApiAuthorizationCode`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `clientCredentialsRes` | [`ClientCredentialsRes`](../../doc/models/client-credentials-res.md) | Required | - |
| `tokenApiRes` | [`TokenApiRes`](../../doc/models/token-api-res.md) | Required | - |
| `refreshTokenRes` | [`RefreshTokenRes`](../../doc/models/refresh-token-res.md) | Required | - |
| `accessToken` | `string` | Required | - |
| `tokenType` | `string` | Required | - |
| `expiresIn` | `number` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |

## Example

```ts
import { TokenApiAuthorizationCode } from 'walmart-apimatic-sdk';

const tokenApiAuthorizationCode: TokenApiAuthorizationCode = {
  clientCredentialsRes: {
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
  },
  tokenApiRes: {
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
  },
  refreshTokenRes: {
    summary: 'Token API - refresh_token',
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
  },
  accessToken: 'eyJraWQiOiIzN2JmOWQ5MS04ZDRkLTQwYjEtODU4NS1mNzhlZDc3MjM4MDQiLCJlbmMiOiJBMjU2R0NNIiwiYWxnIjoiZGlyIn0..bKkYKqJ5CP0Qb2Qz.wQ4TTa2nwL1rbT98BBdbTi_MRNMM0gW_5q8im6uX4olRwYiuOXjaG6TbnnFOK5fT0UzMEJUf-uybalogMH78cHP0ZyL6hONKJOMJ8VK3ThcZ4AUcqrMRBNIMFiAWSTvHJg1y5g-t-WwmZbaD589dMll7-aXG6PPncpeQA1zOyOTaELjDA4O4jimc2_7PnEdc6ETv89AKcnw1J1cPz6BPG9jpyLVX_zEZcQnxbAHYZiSFscFCzdMtpFDrPWIwWuRcV5qRlH4DghHMqKG7V2wqX1VYV_gUvLH5b2y8O6Y0u9nmkBpqTGNiMpWzNE7amFyqKExGk4Jc_ziJdsrj38cSz9a4KtZOrV6E3mN5gFFEQSNAGzrdEv2IdTfWdNgTnHopQecgrlP7EcsrmGh1ARGTWr-e7RaiL8m2Sx5i9odGj5FDJKXiDeohX-KEB-Vc2KJeLxvYAHA7nPT1_pkZDBCfpqq_6GAUBDEbDZ6mJH93TAE1YhFeR_jcdl_23lND9sHKlvHA97-fHAjEVTqu-4wVmFFelGyJD4VIBkieWn94jq_opMiz-RjyYn8Vj-tfdJy8azBNt5NkjjW7Rsque04LsfujrqHDcJHio3ukT5JKwxNv9PoHMxoHnQ5fUdF4pOzt6ZShkki-jSbhileDlClh0ufLSNYgBmy6Fz4wTZWgL-DhJOcv-7Cup95Rx35Wh7XDYTbdz_z_avtfF-f-JS5XyN20Hn-gioWdNA7DNhI1O6s7zKZ2s2iD9eFkprOLGtcJzvNVjrxKZKD6R0hrUUzDXRn95oWlJXfan-OsTNdRypfGWFqIes-n8cBhzVF69LEWIDMr6YfdkRkmCq_p_A.Bvyf-k_rnsiiuf0jGGVXvw',
  tokenType: 'Bearer',
  expiresIn: 900,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```

