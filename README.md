
# Getting Started with Walmart APIs

## Introduction

The price is a fundamental building block for your listing on Walmart.com. You can use the price management APIs to set up and manage the price for a given item, The Walmart Marketplace APIs use OAuth for token-based authentication and authorization.  
We also introduced OAuth 2.0 for solution providers to enable new authorizations using authorization code grant type. Sellers can now connect with solution provider apps seamlessly through this new Walmart's OAuth 2.0 user experience. Refer to the [Guide section](https:///doc/us/mp/us-mp-auth2/#606) for comprehensive instructions. Existing seller connections using the previous authorization method will remain operational.

## Install the Package

Run the following command from your project directory to install the package from npm:

```bash
npm install walmart-apimatic-sdk@0.0.2
```

For additional package details, see the [Npm page for the walmart-apimatic-sdk@0.0.2 npm](https://www.npmjs.com/package/walmart-apimatic-sdk/v/0.0.2).

## Initialize the API Client

**_Note:_** Documentation for the client can be found [here.](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/client.md)

The following parameters are configurable for the API Client:

| Parameter | Type | Description |
|  --- | --- | --- |
| environment | [`Environment`](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/README.md#environments) | The API environment. <br> **Default: `Environment.Production`** |
| timeout | `number` | Timeout for API calls.<br>*Default*: `30000` |
| httpClientOptions | [`Partial<HttpClientOptions>`](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/http-client-options.md) | Stable configurable http client options. |
| unstableHttpClientOptions | `any` | Unstable configurable http client options. |
| logging | [`PartialLoggingOptions`](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/partial-logging-options.md) | Logging Configuration to enable logging |
| basicAuthCredentials | [`BasicAuthCredentials`](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/auth/basic-authentication.md) | The credential object for basicAuth |

The API client can be initialized as follows:

### Code-Based Client Initialization

```ts
import { Client, Environment, LogLevel } from 'walmart-apimatic-sdk';

const client = new Client({
  basicAuthCredentials: {
    username: 'username',
    password: 'password'
  },
  timeout: 30000,
  environment: Environment.Production,
  logging: {
    logLevel: LogLevel.Info,
    logRequest: {
      logBody: true
    },
    logResponse: {
      logHeaders: true
    }
  },
});
```

### Configuration-Based Client Initialization

```ts
import * as path from 'path';
import * as fs from 'fs';
import { Client } from 'walmart-apimatic-sdk';

// Provide absolute path for the configuration file
const absolutePath = path.resolve('./config.json');

// Read the configuration file content
const fileContent = fs.readFileSync(absolutePath, 'utf-8');

// Initialize client from JSON configuration content
const client = Client.fromJsonConfig(fileContent);
```

See the [Configuration-Based Client Initialization](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/configuration-based-client-initialization.md) section for details.

### Environment-Based Client Initialization

```ts
import * as dotenv from 'dotenv';
import * as path from 'path';
import * as fs from 'fs';
import { Client } from 'walmart-apimatic-sdk';

// Optional - Provide absolute path for the .env file
const absolutePath = path.resolve('./.env');

if (fs.existsSync(absolutePath)) {
  // Load environment variables from .env file
  dotenv.config({ path: absolutePath, override: true });
}

// Initialize client using environment variables
const client = Client.fromEnvironment(process.env);
```

See the [Environment-Based Client Initialization](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/environment-based-client-initialization.md) section for details.

## Environments

The SDK can be configured to use a different environment for making API calls. Available environments are:

### Fields

| Name | Description |
|  --- | --- |
| Production | **Default** |

## Authorization

This API uses the following authentication schemes.

* [`basic (Basic Authentication)`](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/auth/basic-authentication.md)

## List of APIs

* [Strategy Collection Id](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/controllers/strategy-collection-id.md)
* [Strategy](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/controllers/strategy.md)
* [Strategies](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/controllers/strategies.md)
* [Wfpreference](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/controllers/wfpreference.md)
* [Incentives](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/controllers/incentives.md)
* [Get Pricing Insights](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/controllers/get-pricing-insights.md)
* [Price](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/controllers/price.md)
* [Repricer Feeds](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/controllers/repricer-feeds.md)
* [Feeds](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/controllers/feeds.md)
* [Feeds ? Feed Type PRICE and PROMOTION](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/controllers/feeds-feed-type-price-and-promotion.md)
* [Feeds ? Feed Type WALMART FUNDED INCENTIVES ENROLLMENT](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/controllers/feeds-feed-type-walmart-funded-incentives-enrollment.md)
* [Feeds ? Feed Type INCENTIVE ENROLLMENT](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/controllers/feeds-feed-type-incentive-enrollment.md)
* [Cppreference](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/controllers/cppreference.md)
* [Detail](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/controllers/detail.md)
* [Token](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/controllers/token.md)
* [Misc](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/controllers/misc.md)

## SDK Infrastructure

### Configuration

* [HttpClientOptions](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/http-client-options.md)
* [RetryConfiguration](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/retry-configuration.md)
* [ProxySettings](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/proxy-settings.md)
* [Configuration-Based Client Initialization](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/configuration-based-client-initialization.md)
* [Environment-Based Client Initialization](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/environment-based-client-initialization.md)
* [PartialLoggingOptions](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/partial-logging-options.md)
* [PartialRequestLoggingOptions](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/partial-request-logging-options.md)
* [PartialResponseLoggingOptions](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/partial-response-logging-options.md)
* [LoggerInterface](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/logger-interface.md)

### HTTP

* [HttpRequest](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/http-request.md)

### Utilities

* [ApiResponse](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/api-response.md)
* [ApiError](https://www.github.com/sdks-io/walmart-apimatic-js-sdk/tree/0.0.2/doc/api-error.md)

