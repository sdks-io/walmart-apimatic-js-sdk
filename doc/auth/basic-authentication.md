
# Basic Authentication



Documentation for accessing and setting credentials for basic.

## Auth Credentials

| Name | Type | Description | Setter |
|  --- | --- | --- | --- |
| username | `string` | - | `username` |
| password | `string` | - | `password` |



**Note:** Auth credentials can be set using `basicAuthCredentials` object in the client.

## Usage Example

### Client Initialization

You must provide credentials in the client as shown in the following code snippet.

```ts
import { Client } from 'walmart-apimatic-sdk';

const client = new Client({
  basicAuthCredentials: {
    username: 'username',
    password: 'password'
  },
});
```


