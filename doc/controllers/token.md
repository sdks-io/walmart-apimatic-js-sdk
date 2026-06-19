# Token

```ts
const tokenApi = new TokenApi(client);
```

## Class Name

`TokenApi`


# Token API

Obtain access tokens for API authentication using OAuth 2.0 by providing Client ID and Client Secret. This endpoint supports multiple grant types for different authentication scenarios - Client Credentials Grant, Authorization Code Grant, Refresh Token Grant.

An access token expires after a certain interval, so you will have to refresh a user's access token. You could use refresh token, obtained from the token API call using authorization code grant type, to get a new access token. <b>Token Lifetimes</b><br /><ul><li><b>Access Token:</b> 15 minutes (900 seconds)</li><li><b>Refresh Token:</b> 1 year (365 days)</li></ul><br /> <a href="https://developer.walmart.com/us-marketplace/docs/get-an-access-token">Get an access token using Token API</a>

<a href="https://developer.walmart.com/us-marketplace/docs/get-started-as-a-seller">Get started as a seller</a>

<a href="https://developer.walmart.com/us-marketplace/docs/get-started-as-a-solution-provider">Get started as a solution provider</a>

<a href="https://developer.walmart.com/us-marketplace/docs/oauth-20-authorization">OAuth2.0 authorization</a>

```ts
async tokenApi(
  wmPartnerId: number,
  wmConsumerChannelType: string,
  wmQosCorrelationId: string,
  wmSvcName: string,
  accept: string,
  grantType: string,
  code: string,
  redirectUri: string,
  refreshToken: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<TokenApiClientCredentials>>
```

## Authentication

This endpoint requires [basic](../../doc/auth/basic-authentication.md)

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `wmPartnerId` | `number` | Header, Required | Partner ID registered in Walmart marketplace to identify a seller account. <br /> This field is required when `grant_type` is `authorization_code` or `refresh_token`. |
| `wmConsumerChannelType` | `string` | Header, Required | A unique ID to track the consumer request by channel. Use the Consumer Channel Type received during onboarding. |
| `wmQosCorrelationId` | `string` | Header, Required | A unique ID that identifies each API call and is used to track and debug issues. Use a randomly generated GUID for this ID. |
| `wmSvcName` | `string` | Header, Required | Specifies the name of the Walmart service being called. |
| `accept` | `string` | Header, Required | - |
| `grantType` | `string` | Form, Required | Type of OAuth2.0 grant requested. <br /> **Available grant types:** `authorization_code`, `refresh_token` and `client_credentials` |
| `code` | `string` | Form, Required | Authorization code returned to your redirect URI, obtained by your client app when the seller authorizes your app to access the seller resource. <br /> This field is required when **grant_type: authorization_code**. |
| `redirectUri` | `string` | Form, Required | Redirect URI must exactly match one of the URIs registered for your client app, which was provided while registering the app. <br /> This field is required when **grant_type: authorization_code**. |
| `refreshToken` | `string` | Form, Required | Refresh token received as response of Authentication API with authorization_code grant type. Use it to exchange for a new access token when the current one expires. <br /> This field is required when **grant_type: refresh_token**. |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`TokenApiClientCredentials`](../../doc/models/token-api-client-credentials.md).

## Example Usage

```ts
const wmPartnerId = 43423324;

const wmConsumerChannelType = 'string';

const wmQosCorrelationId = 'b3261d2d-028a-4ef7-8602-633c23200af6';

const wmSvcName = 'Walmart Marketplace';

const accept = 'application/json';

const grantType = 'client_credentials';

const code = '65CA5DA313A549D49D15D3119D9AD85D';

const redirectUri = 'https://example-client-app.com';

const refreshToken = 'APXcIoTpKMH9OQN.....';

try {
  const response = await tokenApi.tokenApi(
    wmPartnerId,
    wmConsumerChannelType,
    wmQosCorrelationId,
    wmSvcName,
    accept,
    grantType,
    code,
    redirectUri,
    refreshToken
  );

  // Extracting fully parsed response body.
  console.log(response.result);

  // Extracting response status code.
  console.log(response.statusCode);
  // Extracting response headers.
  console.log(response.headers);
  // Extracting response body of type `string | Stream`
  console.log(response.body);
} catch (error) {
  if (error instanceof ApiError) {
    // Extracting response error status code.
    console.log(error.statusCode);
    // Extracting response error headers.
    console.log(error.headers);
    // Extracting response error body of type `string | Stream`.
    console.log(error.body);
  }
}
```

## Example Response *(as JSON)*

```json
{
  "clientCredentialsRes": {
    "summary": "Token API - client_credentials",
    "value": {
      "access_token": "eyJraWQiOiI1MWY3MjM0Ny0wYWY5LTRhZ.....",
      "token_type": "Bearer",
      "expires_in": 900
    }
  },
  "tokenAPIRes": {
    "summary": "Token API - authorization_code",
    "value": {
      "access_token": "eyJraWQiOiI1MWY3MjM0Ny0wYWY5LTRhZ.....",
      "refresh_token": "APXcIoTpKMH9OQN....",
      "token_type": "Bearer",
      "expires_in": 900
    }
  },
  "refreshTokenRes": {
    "summary": "Token API - refresh_token",
    "value": {
      "access_token": "eyJraWQiOiI1MWY3MjM0Ny0wYWY5LTRhZ.....",
      "token_type": "Bearer",
      "expires_in": 900
    }
  },
  "access_token": "eyJraWQiOiIzN2JmOWQ5MS04ZDRkLTQwYjEtODU4NS1mNzhlZDc3MjM4MDQiLCJlbmMiOiJBMjU2R0NNIiwiYWxnIjoiZGlyIn0..bKkYKqJ5CP0Qb2Qz.wQ4TTa2nwL1rbT98BBdbTi_MRNMM0gW_5q8im6uX4olRwYiuOXjaG6TbnnFOK5fT0UzMEJUf-uybalogMH78cHP0ZyL6hONKJOMJ8VK3ThcZ4AUcqrMRBNIMFiAWSTvHJg1y5g-t-WwmZbaD589dMll7-aXG6PPncpeQA1zOyOTaELjDA4O4jimc2_7PnEdc6ETv89AKcnw1J1cPz6BPG9jpyLVX_zEZcQnxbAHYZiSFscFCzdMtpFDrPWIwWuRcV5qRlH4DghHMqKG7V2wqX1VYV_gUvLH5b2y8O6Y0u9nmkBpqTGNiMpWzNE7amFyqKExGk4Jc_ziJdsrj38cSz9a4KtZOrV6E3mN5gFFEQSNAGzrdEv2IdTfWdNgTnHopQecgrlP7EcsrmGh1ARGTWr-e7RaiL8m2Sx5i9odGj5FDJKXiDeohX-KEB-Vc2KJeLxvYAHA7nPT1_pkZDBCfpqq_6GAUBDEbDZ6mJH93TAE1YhFeR_jcdl_23lND9sHKlvHA97-fHAjEVTqu-4wVmFFelGyJD4VIBkieWn94jq_opMiz-RjyYn8Vj-tfdJy8azBNt5NkjjW7Rsque04LsfujrqHDcJHio3ukT5JKwxNv9PoHMxoHnQ5fUdF4pOzt6ZShkki-jSbhileDlClh0ufLSNYgBmy6Fz4wTZWgL-DhJOcv-7Cup95Rx35Wh7XDYTbdz_z_avtfF-f-JS5XyN20Hn-gioWdNA7DNhI1O6s7zKZ2s2iD9eFkprOLGtcJzvNVjrxKZKD6R0hrUUzDXRn95oWlJXfan-OsTNdRypfGWFqIes-n8cBhzVF69LEWIDMr6YfdkRkmCq_p_A.Bvyf-k_rnsiiuf0jGGVXvw",
  "token_type": "Bearer",
  "expires_in": 900
}
```

