# API v1.2

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