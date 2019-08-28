# API v1.2

Please read this entire document before attempting to interact with the SmartPay API. If this is your first time connecting to an external API, you may wish to begin with the [quick start guide](quickstart/tutorial.md).

# How It Works

The SmartPay API accepts queries using a two-phase approach: the authentication handshake and then the actual query itself. In either scenario, the system is queried with a version number, an endpoint (which defines the type of information requested) and a payload containing input parameters (sent by POST), and then returns a resultset.

The URL structure for querying the API is as follows:

```
https://api.smartpay.curexe.com/1-2/authenticate
```

"1-2" represents the version number, and "authenticate" represents the endpoint. All versions and endpoints will be documented here.

# Authentication Phase

The API is queried with a key which is obtained from the Integrate page in the SmartPay web application:

```
{
  api_key: ABC123
}
```

The returned data is either the resultset (in this case a session token), or any errors:


```
{
  result: [
    token: DEF456,
    expires_on: "2018-01-01 12:00:00"
  ]

  errors: [
    "1001": "Invalid key",
  ],
}
```

* Note that this result set is solely illustrative; a token would never be provided if there were errors, only warnings.

Tokens will expire within one hour of issue.

# Query Phase

The token provided in the authentication phase is used as an input parameter to authenticate phase two: the actual data query. The result set may look something like this:


```
{
  page: 1,
  total_pages: 3,
  result: [
    ...
  ]
}
```

## Overview

<img src="assets/endpoints.png">

## Endpoints

### Authentication

- [authenticate](authenticate/authenticate.md)

### Consumers

- [/get_consumers](consumers/get_consumers.md)
- [/create_consumer](consumers/create_consumer.md)
- [/modify_consumer](consumers/modify_consumer.md)
- [/delete_consumer](consumers/delete_consumer.md)

### Orders

Orders are a grouping of invoices.  Each orders has at least 1 invoice initially (a single amount to be collected from the consumer).  Future implementations of recurring billing will include multiple invoices per order.

- [/get_orders](orders/get_orders.md)

### Invoices

Invoices represent the amount to be collected from the consumer, when it was received, and if there was any problems with processing the payment.

- [/get_invoices](invoices/get_invoices.md)

### Webhooks

Webhooks allow you to subscribe to have status updates sent to a url when certain actions occur within SmartPay.

- [/get_webhooks](webhooks/get_webhooks.md)
- [/create_webhook](webhooks/create_webhook.md)
- [/modify_webhook](webhooks/modify_webhook.md)
- [/delete_webhook](webhooks/delete_webhook.md)