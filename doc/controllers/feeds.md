# Feeds

```ts
const feedsApi = new FeedsApi(client);
```

## Class Name

`FeedsApi`


# Update Bulk Prices Legacy

Updates prices in bulk.

In one Feed you can update up to 10,000 items in bulk. To ensure optimal Feed processing time, we recommend sending no more than 1000 items in one Feed and keeping the Feed sizes below 10 MB.

The price sequence guarantee is observed by the bulk price update functionality, subject to the following rules:

The timestamp used to determine precedence is passed in the request headers. All price updates in the feed are considered to have the same timestamp. The timestamp in the XML file is used only for auditing.
You can send a single SKU multiple times in one Feed. If a SKU is repeated in a Feed, the price will be set for that SKU on Walmart.com, but there is no guarantee as to which SKU's price within that feed will be used.
This API should be used in preference to the update a price. It should be called no sooner than 24 hours after a new item is set up and a wpid (Walmart Part ID) is available. Thereafter, the bulk price update has an service level agreement (SLA) of 15 minutes.

After the update is submitted, wait for at least five minutes before verifying whether the bulk price update was successful. Individual SKU price update success or failure is only available after the entire feed is processed.

If a SKU's price update fails (for example, multiple price updates were sent for the same SKU in a single feed), an error will be returned.

<b>You can download the request body sample from <a href="/file/mp/us/price-feed.zip">here</a></b>

:information_source: **Note** This endpoint does not require authentication.

```ts
async updateBulkPricesLegacy(
  feedType: string,
  wmSecAccessToken: string,
  wmConsumerChannelType: string,
  wmQosCorrelationId: string,
  wmSvcName: string,
  accept: string,
  file: FileWrapper,
  requestOptions?: RequestOptions
): Promise<ApiResponse<Json1>>
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `feedType` | `string` | Query, Required | The feed Type |
| `wmSecAccessToken` | `string` | Header, Required | The access token retrieved in the Token API call |
| `wmConsumerChannelType` | `string` | Header, Required | A unique ID to track the consumer request by channel. Use the Consumer Channel Type received during onboarding |
| `wmQosCorrelationId` | `string` | Header, Required | A unique ID which identifies each API call and used to track and debug issues; use a random generated GUID for this ID |
| `wmSvcName` | `string` | Header, Required | Walmart Service Name |
| `accept` | `string` | Header, Required | - |
| `file` | `FileWrapper` | Form, Required | Feed file to upload |
| `requestOptions` | `RequestOptions \| undefined` | Optional | Pass additional request options. |

## Response Type

**200**

This method returns an [`ApiResponse`](../../doc/api-response.md) instance. The `result` property of this instance returns the response data which is of type [`Json1`](../../doc/models/json-1.md).

## Example Usage

```ts
const feedType = 'CPT_SELLER_ELIGIBILITY';

const wmSecAccessToken = 'eyJraWQiOiIzZjVhYTFmNS1hYWE5LTQzM.....';

const wmConsumerChannelType = 'string';

const wmQosCorrelationId = 'b3261d2d-028a-4ef7-8602-633c23200af6';

const wmSvcName = 'Walmart Service Name';

const accept = 'application/json';

const file = new FileWrapper(fs.createReadStream('dummy_file'));

try {
  const response = await feedsApi.updateBulkPricesLegacy(
    feedType,
    wmSecAccessToken,
    wmConsumerChannelType,
    wmQosCorrelationId,
    wmSvcName,
    accept,
    file
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
  "feedId": "14066B6642344B76A8B77AC094F8C63B@AVMBAgA"
}
```

