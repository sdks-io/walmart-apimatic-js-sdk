# Wfpreference

```ts
const wfpreferenceApi = new WfpreferenceApi(client);
```

## Class Name

`WfpreferenceApi`


# Update Walmart-Funded Incentives Enrollment for All Items

Updates the enrollment status of all items in the Walmart-funded incentives program. By default, all items are auto-enrolled in Walmart-funded incentives, meaning that eligible items are automatically included in these programs to benefit from price reductions funded by Walmart.

If you wish to permanently turn off Walmart-funded incentives for all items in your catalog, you can use this API to set the Walmart-funded incentives program status to `OFF`. The default value of this variable is `ON`. Any changes to preferences will lock in (disable) the preference option for a period of 4 hours, as indicated by the `isDisabled` response field of the API.

For more information and usage examples, refer to the <a href="https://developer.walmart.com/us-marketplace/docs/manage-enrollment-all-items-in-walmart-funded-incentives">Pricing API Guide</a>

:information_source: **Note** This endpoint does not require authentication.

```ts
async updateWalmartFundedIncentivesEnrollmentForAllItems(
  autoEnrollEnabled: boolean,
  wmSecAccessToken: string,
  wmConsumerChannelType: string,
  wmQosCorrelationId: string,
  wmSvcName: string,
  accept: string,
  requestOptions?: RequestOptions
): Promise<ApiResponse<SuccessfulOperation4>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `autoEnrollEnabled` | `boolean` | Query, Required | Specify the boolean for enabling auto enrollment. Examples of the allowed values are `true` or `false`. |
| `wmSecAccessToken` | `string` | Header, Required | Access token obtained from the Token API. This is required for authenticating requests to Walmart Marketplace APIs. |
| `wmConsumerChannelType` | `string` | Header, Required | A unique ID to identify the consumer request by channel. Use the Consumer Channel Type received during onboarding. |
| `wmQosCorrelationId` | `string` | Header, Required | A unique ID that identifies each API call and is used to track and debug issues. Use a randomly generated GUID for this ID. |
| `wmSvcName` | `string` | Header, Required | Specifies the name of the Walmart service being called. |
| `accept` | `string` | Header, Required | - |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`SuccessfulOperation4`](../../doc/models/successful-operation-4.md).

## Example Usage

```ts
const autoEnrollEnabled = true;

const wmSecAccessToken = 'eyJraWQiOiIzZjVhYTFmNS1hYWE5LTQzM.....';

const wmConsumerChannelType = 'string';

const wmQosCorrelationId = 'b3261d2d-028a-4ef7-8602-633c23200af6';

const wmSvcName = 'Walmart Marketplace';

const accept = 'application/json';

try {
  const response = await wfpreferenceApi.updateWalmartFundedIncentivesEnrollmentForAllItems(
    autoEnrollEnabled,
    wmSecAccessToken,
    wmConsumerChannelType,
    wmQosCorrelationId,
    wmSvcName,
    accept
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
  "autoEnrollEnabled": true,
  "isDisabled": true
}
```

